1. Run the commands on your terminal to encode the passwords

```bash
echo -n "your-root-password" | base64
echo -n "your-username" | base64
echo -n "your-user-password" | base64
```

2. Run following command to decode password

```bash
echo "YWRtaW4xMjM=" | base64 --decode
```

3. Sign into mysql database by using password configured as secret

```bash
kubectl exec -it <pod-name> -c mysql -- mysql -u root -p
```

4. Exit the mysql prompt with 

```bash
\q
```