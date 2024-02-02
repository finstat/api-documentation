``` php
function ComputeVerificationHash($apiKey, $privateKey, $$hashParam)
{
    $data = sprintf("SomeSalt+%s+%s++%s+ended", $apiKey, $privateKey, $hashParam);
    return hash('sha256', $data);
}
```