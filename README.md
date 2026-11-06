# Keys Without Trust Assumptions

> **QKD + Post-Quantum Cryptography (PQC) for quantum-era networks**

This project examines how Quantum Key Distribution (QKD) and Post-Quantum
Cryptography can work together to protect network key establishment. It treats
QKD as a networking and systems-integration challenge: generating keys is only
part of the problem; those keys must also be authenticated, delivered, and
consumed by existing protocols while accounting for distance, key rate, trust,
latency, and availability.

**Author:** Truong Phat Tu  
**Course:** Computer Networks I (CN1)  
**Track:** Emerging Networking Technology / Network Security  
**Course section, semester, sponsor, and institution:** To be completed

## Project links

- **GitHub repository:** To be added
- **LinkedIn post:** To be added
- **YouTube post/video:** To be added

## Project overview

Conventional secure sessions use public-key key-exchange mechanisms whose
security depends on computational assumptions that a sufficiently capable
quantum computer could undermine. This creates a “harvest now, decrypt later”
risk for information that needs to remain confidential for years.

The project’s central question is: **How can quantum-derived keys reach
applications and network protocols, and what are the costs in latency,
throughput, topology, and trust?**

The proposed near-term direction is a hybrid architecture:

- **PQC** provides scalable key establishment and authentication over ordinary
  IP networks.
- **QKD** can supply additional key material on selected links where the
  necessary physical infrastructure is available.
- A session protocol combines independent key contributions so that one
  compromised component does not, by itself, compromise the session.

QKD generates key material; it is not an encryption algorithm or a replacement
for IP networking. Symmetric cryptography such as AES still protects bulk data.

## How the architecture works

1. QKD endpoints exchange quantum signals and compare measurement bases over a
   **public but authenticated** classical channel.
2. They estimate the quantum bit error rate (QBER). If it exceeds the
   protocol’s acceptable threshold, key generation aborts.
3. Error reconciliation and privacy amplification produce matching secret
   keys, which are stored in local Key Management Entities (KMEs).
4. An application requests key material through the ETSI GS QKD 014 REST API.
   The peer application uses a `key_ID` to retrieve its matching key from its
   local KME; the secret key itself is not sent across the public network.
5. A consuming protocol such as IKEv2 can mix key contributions from classical,
   post-quantum, and QKD sources.

QKD’s physical channel does not route like ordinary IP traffic. Current
long-distance deployments may depend on trusted relay nodes, which hold
intermediate key material and therefore introduce physical and operational
trust requirements.

## Networking concepts explored

The poster connects QKD/PQC integration to:

- Protocol layering, handshakes, and state machines
- Encapsulation and key delivery through an API
- Throughput limits, delay, buffering, and key-pool queuing
- Error control and QBER
- Admission control and key-pool exhaustion
- Routing, topology, trust boundaries, and network availability
- Separation of quantum, key-management, and data planes

## Findings and limitations

- QKD’s security properties rely on protocol and device assumptions, and QKD
  still requires authenticated classical communication.
- QKD does not eliminate trust: trusted relays and physical infrastructure
  can become trust points.
- Fiber loss limits distance and secret-key rate; key-pool exhaustion can
  affect service availability.
- QKD requires specialized hardware and is not a general-purpose replacement
  for scalable, software-based PQC.
- The project characterizes QKD as **emerging, actively standardized, and
  deployed in limited niches**; PQC is the more broadly deployable near-term
  foundation. The hybrid approach is a direction for selected high-value links,
  not a claim that QKD is appropriate everywhere.

## Project materials

- [Research poster (PDF)](./QKD_PostQuantum_BLAST_Research_Poster.pdf)
- [Research poster (PowerPoint)](./QKD_PostQuantum_BLAST_Research_Poster.pptx)
- [Poster content and research notes](./QKD_PostQuantum_BLAST_Poster_Content.txt)
- [Project abstract (PDF)](./QKD_PostQuantum_BLAST_Abstract.pdf)
- [Project abstract (Word)](./QKD_PostQuantum_BLAST_Abstract.docx)
- [LinkedIn post draft](./LINKEDIN_POST.md)
- [YouTube post draft](./YOUTUBE_POST.md)

## References

The following references are reproduced from the poster content. The poster
master still contains incomplete bibliographic fields for some cited items;
complete and verify those entries before final academic submission.

1. C. H. Bennett and G. Brassard, “Quantum cryptography: Public key
   distribution and coin tossing,” in *Proc. IEEE Int. Conf. Comput., Syst.
   Signal Process.*, Bangalore, India, Dec. 1984, pp. 175–179.
2. A. K. Ekert, “Quantum cryptography based on Bell’s theorem,” *Physical
   Review Letters*, vol. 67, no. 6, pp. 661–663, Aug. 1991.
3. *Quantum Key Distribution (QKD); Protocol and Data Format of REST-Based Key
   Delivery API*, ETSI GS QKD 014 V1.1.1, European Telecommunications
   Standards Institute, Feb. 2019.
4. *Module-Lattice-Based Key-Encapsulation Mechanism Standard*, FIPS PUB 203,
   National Institute of Standards and Technology, Aug. 2024.
5. *Module-Lattice-Based Digital Signature Standard*, FIPS PUB 204, National
   Institute of Standards and Technology, Aug. 2024.
6. C. Tjhai et al., “Mixing preshared keys in the Internet Key Exchange
   Protocol Version 2 (IKEv2) for post-quantum security,” IETF RFC 8784,
   Jun. 2020.
7. C. Tjhai et al., “Multiple key exchanges in the Internet Key Exchange
   Protocol Version 2 (IKEv2),” IETF RFC 9370, May 2023.
8. *Overview on Networks Supporting Quantum Key Distribution*, ITU-T
   Recommendation Y.3800, International Telecommunication Union, Oct. 2019.
9. S.-K. Liao et al., “Satellite-to-ground quantum key distribution,”
   *Nature*, vol. 549, no. 7670, pp. 43–47, Sep. 2017.
10. Y.-A. Chen et al., “An integrated space-to-ground quantum communication
    network over 4,600 kilometres,” *Nature*, vol. 589, no. 7841,
    pp. 214–219, Jan. 2021.
11. M. Lucamarini et al., “Overcoming the rate–distance limit of quantum key
    distribution without quantum repeaters,” *Nature*, vol. 557, no. 7705,
    pp. 400–403, May 2018.
12. M. Peev et al., “The SECOQC quantum key distribution network in Vienna,”
    *New Journal of Physics*, vol. 11, no. 7, art. no. 075001, Jul. 2009.
13. M. Sasaki et al., “Field test of quantum key distribution in the Tokyo QKD
    Network,” *Optics Express*, vol. 19, no. 11, pp. 10387–10409, May 2011.
14. V. Scarani et al., “The security of practical quantum key distribution,”
    *Reviews of Modern Physics*, vol. 81, no. 3, pp. 1301–1350, Sep. 2009.
15. F. Xu et al., “Secure quantum key distribution with realistic devices,”
    *Reviews of Modern Physics*, vol. 92, no. 2, art. no. 025002, May 2020.

### Links

- **GitHub repository:** [repository URL](http://github.com/sturekev/cyber_sec_blast)
- **LinkedIn post:** [LinkedIn post URL](https://lnkd.in/p/gB7r9BAk)
- **Youtube video:** [Video](https://youtu.be/bx6_IJhoCcw)