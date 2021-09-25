---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: SMTP アカウントに使用する認証方法を指定します。
ms.openlocfilehash: b98b736f98bb1f66a3c8e4a3bf852f2bc9c037f0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601143"
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

