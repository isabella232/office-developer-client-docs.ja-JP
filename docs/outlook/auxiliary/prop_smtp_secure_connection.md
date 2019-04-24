---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: SMTP アカウントに使用する暗号化された接続の種類を指定します。
ms.openlocfilehash: 67eae5c9c5ca1b7f664ceaac0463ef3f3c9a291a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328330"
---
# <a name="propsmtpsecureconnection"></a>PROP_SMTP_SECURE_CONNECTION

SMTP アカウントに使用する暗号化された接続の種類を指定します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|識別子:  <br/> |0x020a  <br/> |
|プロパティの種類:  <br/> |PT_DWORD  <br/> |
|プロパティタグ:  <br/> |0x020A0003  <br/> |
|接続  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>解説

この値には、次の定数のいずれかを指定できます。 値については、「 [Constants (Account management API)](constants-account-management-api.md) 」を参照してください。 
  
|**Constants**|**説明**|
|:-----|:-----|
|**ENCRYPT_CONN_NO_SECURITY** <br/> |暗号化は使用しないでください。  <br/> |
|**ENCRYPT_CONN_SSL** <br/> |Secure Socket Layer (SSL) 暗号化を使用します。  <br/> |
|**ENCRYPT_CONN_TLS** <br/> |TLS (Transport Layer Security) 暗号化と認証プロトコルを使用します。  <br/> |
|**ENCRYPT_CONN_AUTO** <br/> |メールサーバーでサポートされている暗号化方法を自動的に検出して使用します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [POP3 アカウントのメッセージ ダウンロードの管理](managing-message-downloads-for-pop3-accounts.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)

