---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: アカウントのアドレス帳エントリ ID を取得または設定します。
ms.openlocfilehash: 9d926b5b68fb41962946700f585d6a3629aacd25
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601136"
---
# <a name="prop_mapi_identity_entryid"></a>PROP_MAPI_IDENTITY_ENTRYID

アカウントのアドレス帳エントリ ID を取得または設定します。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccount」を参照してください](iolkaccount.md)。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x2002  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|プロパティ タグ:  <br/> |0x20020102  <br/> |
|アクセス:  <br/> |読み取り/書き込み  <br/> |
   
## <a name="remarks"></a>注釈

 **PROP \_MAPI \_ IDENTITY \_ ENTRYID は** 、すべてのアカウントに存在するとは見なされません。 たとえば、SMTP/POP3 Exchangeアカウントの場合、PROP **\_ MAPI IDENTITY \_ \_ ENTRYID** を設定し、PROP ACCT_USER_EMAIL_ADDR を設定することはできませんが、SMTP/POP3 アカウントの場合は、状況が元に戻されます。 [ \_](prop_acct_user_email_addr.md) **PROP \_MAPI_IDENTITY_ENTRYID** は [、IMAPISession::QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx)で _lppEntryID_ によって返される値に似たエントリ ID を返します。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)

