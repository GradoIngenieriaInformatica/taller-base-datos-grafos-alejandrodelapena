MATCH (p:Persona)-[:USA_TECNOLOGIA]->(t:Tecnologia)
WITH p, collect(t.nombre) AS tecnologias, COUNT(t) AS total
WHERE total > 1
RETURN p.nombre, tecnologias