---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: アカウントの電子メール アドレスを指定します。
ms.openlocfilehash: 3115098fab145194f4a2bb1333e4dd625dfc55c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557065"
---
# <a name="prop_acct_user_email_addr"></a>PROP_ACCT_USER_EMAIL_ADDR

アカウントの電子メール アドレスを指定します。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccount」を参照してください](iolkaccount.md)。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x000C  <br/> |
|プロパティの種類:  <br/> |PT_UNICODE  <br/> |
|プロパティ タグ:  <br/> |0x000C001F  <br/> |
|アクセス:  <br/> |読み取り/書き込み  <br/> |
   
## <a name="remarks"></a>注釈

 **PROP_ACCT_USER_EMAIL_ADDR** アカウントに存在するとは見なされません。 たとえば、SMTP/POP3 Exchangeの場合、PROP_MAPI_IDENTITY_ENTRYIDがPROP_ACCT_USER_EMAIL_ADDRを持つ可能性がありますが、この状態は元に戻されます。 [](prop_mapi_identity_entryid.md)
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)

