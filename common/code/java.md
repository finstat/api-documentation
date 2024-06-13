``` java
public static String ComputeVerificationHash(String apiKey, String privateKey, String parameter) throws NoSuchAlgorithmException, UnsupportedEncodingException {
    MessageDigest digest = MessageDigest.getInstance("SHA-256");
    byte[] hash = 
    digest.digest("SomeSalt+".concat(apiKey)concat("+").concat(privateKey).concat("++").concat(parameter).concat("+ended").getBytes());
    StringBuilder hashString = new StringBuilder();
    for (byte x : hash) {
        hashString.append(String.format("%02x", x));
    }
    return hashString.toString();
}
```