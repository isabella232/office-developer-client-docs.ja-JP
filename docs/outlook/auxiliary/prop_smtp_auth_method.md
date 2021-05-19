---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: SMTP アカウントに使用する認証方法を指定します。
ms.openlocfilehash: bb5adeb1fe73ed8b7ab69ca584215b44e1a9e4b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434642"
---
# <a name="prop_smtp_auth_method"></a>PROP_SMTP_AUTH_METHOD

SMTP アカウントに使用する認証方法を指定します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|識別子:  <br/> |0x0208  <br/> |
|プロパティの種類:  <br/> |PT_DWORD  <br/> |
|プロパティ タグ:  <br/> |0x02080003  <br/> |
|アクセス:  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

値は、次の定数のビットマスクです。 値 [については、「定数 (アカウント管理 API)」](constants-account-management-api.md) を参照してください。 
  
- **SMTP_AUTH_SAME_AS_POP** とは、受信メール サーバーと同じ資格情報を使用 [PROP_INET_USERおよび](prop_inet_user.md)PROP_INET_PASSWORD。 [](prop_inet_password.md)
    
- **SMTP_AUTH_USER_PASS** とは、ユーザーおよびユーザーが提供する資格情報を [PROP_SMTP_USER意味](prop_smtp_user.md)[PROP_SMTP_PASSWORD。](prop_smtp_password.md)
    
- **SMTP_AUTH_RECEIVE_BEFORE_SEND** は、メールを送信する前に受信メール サーバーにログオンするユーザーを要求する方法を意味します。 
    
## <a name="see-also"></a>関連項目

- [POP3 アカウントのメッセージ ダウンロードの管理](managing-message-downloads-for-pop3-accounts.md)  
- [定数 (アカウント管理 API)](constants-account-management-api.md)

