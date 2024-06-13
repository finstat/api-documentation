``` csharp
public static string ComputeVerificationHash(string apiKey, string privateKey, string hashParam)
{
    byte[] bytes = Encoding.UTF8.GetBytes(string.Format("SomeSalt+{0}+{1}++{2}+ended", apiKey, privateKey, hashParam));
    SHA256Managed hashstring = new SHA256Managed();
    byte[] hash = hashstring.ComputeHash(bytes);
    StringBuilder hashString = new StringBuilder();
    foreach (byte x in hash)
    {
        hashString.Append(String.Format("{0:x2}", x));
    }
    return hashString.ToString();
}
```