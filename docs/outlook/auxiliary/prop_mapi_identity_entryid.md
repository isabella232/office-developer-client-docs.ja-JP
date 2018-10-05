---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: 取得または、アカウントのアドレス帳のエントリ ID を設定します。
ms.openlocfilehash: 2352f64b46e9884e95b7bf1f3693321f7cd224ca
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400349"
---
# <a name="propmapiidentityentryid"></a>PROP_MAPI_IDENTITY_ENTRYID

取得または、アカウントのアドレス帳のエントリ ID を設定します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x2002  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|プロパティ タグ。  <br/> |0x20020102  <br/> |
|アクセス:  <br/> |値の取得および設定が可能です。  <br/> |
   
## <a name="remarks"></a>備考

 **プロペラ\_MAPI\_の ID\_エントリ ID**のすべてのアカウントの存在ではありません。 たとえば、Exchange アカウントがある**プロペラ\_MAPI\_の ID\_ENTRYID**設定ではなく[プロペラ\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md)、SMTP と POP3 アカウントの場合は、逆です。 **プロペラ\_MAPI_IDENTITY_ENTRYID** [IMAPISession::QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx)の_lppEntryID_によって返される値を次のようなエントリ ID を返します。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)

