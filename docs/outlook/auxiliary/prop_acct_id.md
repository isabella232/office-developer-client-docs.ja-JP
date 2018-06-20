---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: アカウントが作成されるプロファイル内のアカウントを一意に識別する識別子を返します。
ms.openlocfilehash: a4ae193b89132ea718e16aec82f592205f9771c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799566"
---
# <a name="propacctid"></a>PROP_ACCT_ID

アカウントが作成されるプロファイル内のアカウントを一意に識別する識別子を返します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x0001  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|プロパティ タグ。  <br/> |0x00010003  <br/> |
|アクセス:  <br/> |値の取得のみ可能です。  <br/> |
   
## <a name="remarks"></a>備考

[IOlkAccount::GetProp](iolkaccount-getprop.md)を使用してこのプロパティを取得します。 クライアントがこのプロパティを設定しようとすると、このプロパティは**E_OLK_PROP_READ_ONLY**を返します。 
  
このプロパティとは異なる[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md)の値がありますが、アカウントが作成されたときのプロファイル内のすべてのアカウント間でのみ一意な点で**プロペラ\_ACCT_MINI_UID**内のアカウントを一意に識別し、アカウントが作成されたプロファイルの外側です。 2 台目のコンピューター、および**PROP_ACCT_MINI_UID**のプロファイルにアカウントを使用して別の Outlook プロファイルで 2 つ目のコンピューター上にこれらのプロパティを含むメッセージを移動して、可能な限り、 **PROP_ACCT_ID**のアカウントの別のセットとの競合します。元のプロファイルでは、元のアカウントを一意に識別できます。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)  
- [定数 (アカウント管理 API)](constants-account-management-api.md)

