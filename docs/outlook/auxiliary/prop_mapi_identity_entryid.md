---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: アカウントのアドレス帳エントリ ID を取得または設定します。
ms.openlocfilehash: 2352f64b46e9884e95b7bf1f3693321f7cd224ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326433"
---
# <a name="propmapiidentityentryid"></a>PROP_MAPI_IDENTITY_ENTRYID

アカウントのアドレス帳エントリ ID を取得または設定します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x2002  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|プロパティタグ:  <br/> |0x20020102  <br/> |
|接続  <br/> |読み取り/書き込み  <br/> |
   
## <a name="remarks"></a>解説

 **PROP\_MAPI\_id\_の ENTRYID**は、すべてのアカウントに存在するとは想定されていません。 たとえば、Exchange アカウントでは、prop [\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md)ではなく、 **prop\_\_MAPI\_IDENTITY ENTRYID**が設定されている場合がありますが、SMTP/POP3 アカウントでは、状況は逆転しています。 **PROP\_MAPI_IDENTITY_ENTRYID**は、 [imapisession:: queryidentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx)の_lppentryid_によって返される値に似たエントリ ID を返します。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)

