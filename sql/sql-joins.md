# Joins

## Inner join

The INNER JOIN keyword selects records that have matching values in both tables.

I want to see all users with a favorite yoga pose

```sql
SELECT users.name, poses.name
FROM users
INNER JOIN poses
ON users.favorite_pose_id = poses.id;
```

## Left join

The LEFT JOIN keyword returns all records from the left table (users), and the matched records from the right table (yoga poses). The result is NULL from the right side, if there is no match.

I want to see all users even if they don't have a favorite yoga pose (Ben)

```sql
SELECT users.name, poses.name
FROM users
LEFT JOIN poses
ON users.favorite_pose_id = poses.id;
```

## Right join

The RIGHT JOIN keyword returns all records from the right table (yoga poses), and the matched records from the left table (users). The result is NULL from the left side, when there is no match.

I want to see all yoga poses even if no users like them!

```sql
SELECT users.name, poses.name
FROM users
RIGHT JOIN poses
ON users.favorite_pose_id = poses.id;
```

## Outer join

The FULL OUTER JOIN keyword returns all records when there is a match in the left (users) or the right (yoga poses) table records.

I want to see all users and all poses.

```sql
SELECT users.name, poses.name
FROM users
FULL OUTER JOIN poses
ON users.favorite_pose_id = poses.id;
```
