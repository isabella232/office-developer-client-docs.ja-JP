---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: アカウントの電子メール アドレスを指定します。
ms.openlocfilehash: 115941fdf2fdec01da8d6bc1320ac6cdc0930ffa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436777"
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

