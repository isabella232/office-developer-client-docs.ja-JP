---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: アカウントの電子メール アドレスを指定します。
ms.openlocfilehash: 7d0bbba2dcb104326c360da6a10f3e19d1740e46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799571"
---
# <a name="propacctuseremailaddr"></a>PROP_ACCT_USER_EMAIL_ADDR

アカウントの電子メール アドレスを指定します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x000C  <br/> |
|プロパティの種類:  <br/> |PT_UNICODE  <br/> |
|プロパティ タグ。  <br/> |0x000C001F  <br/> |
|アクセス:  <br/> |値の取得および設定が可能です。  <br/> |
   
## <a name="remarks"></a>備考

 **PROP_ACCT_USER_EMAIL_ADDR**は、すべてのアカウントが存在するように想定されていません。 [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md)がない**PROP_ACCT_USER_EMAIL_ADDR**、たとえば、Exchange アカウントがある、SMTP と POP3 アカウントの中にこの状況が一変します。
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)

