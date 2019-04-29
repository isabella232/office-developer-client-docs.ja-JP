---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: アカウントの電子メールアドレスを指定します。
ms.openlocfilehash: 115941fdf2fdec01da8d6bc1320ac6cdc0930ffa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436777"
---
# <a name="propacctuseremailaddr"></a>PROP_ACCT_USER_EMAIL_ADDR

アカウントの電子メールアドレスを指定します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x000c  <br/> |
|プロパティの種類:  <br/> |PT_UNICODE  <br/> |
|プロパティタグ:  <br/> |0x000c001f  <br/> |
|接続  <br/> |読み取り/書き込み  <br/> |
   
## <a name="remarks"></a>注釈

 **PROP_ACCT_USER_EMAIL_ADDR**は、すべてのアカウントに存在するとは想定されていません。 たとえば、Exchange アカウントは[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md)を持つことはできますが、 **PROP_ACCT_USER_EMAIL_ADDR**はできませんが、SMTP/POP3 アカウントの場合は、状況を逆にします。
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)

