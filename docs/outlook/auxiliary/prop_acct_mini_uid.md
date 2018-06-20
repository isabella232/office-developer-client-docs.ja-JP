---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Outlook プロファイル間で一意であるアカウントの識別子を返します。
ms.openlocfilehash: 9b2e30c0f57a54af219e68a8c2fe91e5dba4ddbe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799567"
---
# <a name="propacctminiuid"></a>PROP_ACCT_MINI_UID

Outlook プロファイル間で一意であるアカウントの識別子を返します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x0003  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|プロパティ タグ。  <br/> |0x00030003  <br/> |
|アクセス:  <br/> |値の取得のみ可能です。  <br/> |
   
## <a name="remarks"></a>備考

[IOlkAccount::GetProp](iolkaccount-getprop.md)を使用してこのプロパティを取得します。 クライアントがこのプロパティを設定しようとすると、このプロパティは**E_OLK_PROP_READ_ONLY**を返します。 
  
このプロパティとは異なる[PROP_ACCT_ID](prop_acct_id.md)の値は、アカウントが作成されたプロファイルの内外でのアカウントを一意に識別**PROP_ACCT_ID**はその 1 つのプロファイル内のすべてのアカウント間でのみ一意ですが、そのアカウントが作成されました。 別の Outlook プロファイルとアカウントの別のセットを別のコンピューター上にこれらのプロパティを含むメッセージを移動すると、 **PROP_ACCT_MINI_UID**は元のプロファイルでは、元のアカウントを一意に識別することができます。 ただし、 **PROP_ACCT_ID**可能性がある競合する可能性が 2 番目のコンピューターのプロファイルにアカウントを使用しています。 
  
## <a name="see-also"></a>関連項目

- [PROP_ACCT_ID](prop_acct_id.md)  
- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)

