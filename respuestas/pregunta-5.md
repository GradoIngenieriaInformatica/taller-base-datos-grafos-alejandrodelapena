MATCH (p:Persona)-[:VIVE_EN]->(c1:Ciudad),
      (p)-[:AMIGO_DE]->(amigo:Persona)-[:VIVE_EN]->(c2:Ciudad)
WHERE c1 <> c2
RETURN DISTINCT p.nombre, amigo.nombre