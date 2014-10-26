 # Sengrid API

Haskell utility for sending Email with Sendgrid

You will need a Sendgrid username and password to use this library.

```haskell

import qualified Network.Sendgrid.Api as Sendgrid

message = SendGrid.EmailMessage { to = "owain@owainlewis.com"
                                , from = "noreply@vacancy.io"
                                , subject = "Hello World"
                                , text = "Oh Hai!" }

main = do
    r <- SendGrid.sendEmail (Authentication "USERNAME" "PASSWORD") message
    return $ responseBody r

```
