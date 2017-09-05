## Overheid model description
# ===========================

ro:Overheid
  domain:
  - naamOverheid
  - overheidsCode   (CBS-code) (vorm: 4 cijfers. Ingeval deelgemeente/stadsdeel: CBS-code gemeente.)
    - ro:code       # e.g. "s100"

  sub-classes:
  - OverheidDomain
  - NationaleOverheid
  - ProvincialeOverheid
  - GemeentelijkeOverheid
