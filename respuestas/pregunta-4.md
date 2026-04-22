MATCH (p:Persona)-[:PARTICIPA_EN]->(:Proyecto),
      (p)-[:TRABAJA_EN]->(:Empresa)
RETURN DISTINCT p.nombre