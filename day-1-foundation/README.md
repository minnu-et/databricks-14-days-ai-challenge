# Day 1 – Platform Setup & First Steps

Day 1 focused on understanding Databricks and Spark fundamentals using real data.

---

## 📚 What I Learned

- Why Databricks is preferred over Pandas for large datasets
- Difference between Workspace and Volumes
- Spark’s lazy execution model
- Why schema handling is critical in Spark
- How Lakehouse architecture simplifies data platforms

---

## 🧪 Spark Basics Practiced

```python
data = [("iPhone", 999), ("Samsung", 799), ("MacBook", 1299)]
df = spark.createDataFrame(data, ["product", "price"])
df.show()

df.filter(df.price > 1000).show()
