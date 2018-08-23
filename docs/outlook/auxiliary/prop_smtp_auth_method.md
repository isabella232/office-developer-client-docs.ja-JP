---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: SMTP アカウントに使用する認証方法を指定します。
ms.openlocfilehash: 0c52f1eeca8f7ac3e63cccf712dd672c2247be6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799583"
---
# <a name="propsmtpauthmethod"></a>PROP_SMTP_AUTH_METHOD

SMTP アカウントに使用する認証方法を指定します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|識別子:  <br/> |0x0208  <br/> |
|プロパティの種類:  <br/> |PT_DWORD  <br/> |
|プロパティ タグ。  <br/> |0x02080003  <br/> |
|アクセス:  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

値は、以下の定数のビットマスクです。 その値の[定数 (アカウント管理 API)](constants-account-management-api.md)を参照してください。 
  
- **SMTP_AUTH_SAME_AS_POP**は、 [PROP_INET_USER](prop_inet_user.md)と[PROP_INET_PASSWORD](prop_inet_password.md)によって提供されるように、受信メール サーバーと同じ資格情報を使用してを意味します。
    
- **SMTP_AUTH_USER_PASS**は、 [PROP_SMTP_USER](prop_smtp_user.md)と[PROP_SMTP_PASSWORD](prop_smtp_password.md)によって提供された資格情報を使用することを意味します。
    
- **SMTP_AUTH_RECEIVE_BEFORE_SEND**では、メールを送信する前に受信メール サーバーにログオンするユーザーを要求することを意味します。 
    
## <a name="see-also"></a>関連項目

- [POP3 アカウントのメッセージ ダウンロードの管理](managing-message-downloads-for-pop3-accounts.md)  
- [定数 (アカウント管理 API)](constants-account-management-api.md)

