---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: アカウントの既定の配信ストアのエントリ ID を表します。
ms.openlocfilehash: d803c539ec99da4d7fb31063f48237788f3ac3d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418898"
---
# <a name="prop_acct_delivery_store"></a>PROP_ACCT_DELIVERY_STORE

アカウントの既定の配信ストアのエントリ ID を表します。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccount」を参照してください](iolkaccount.md)。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x0018  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|プロパティ タグ:  <br/> |0x00180102  <br/> |
|アクセス:  <br/> |読み取り/書き込み  <br/> |
   
## <a name="remarks"></a>注釈

[IOlkAccount::GetProp](iolkaccount-getprop.md)または[IOlkAccount::SetProp](iolkaccount-setprop.md)をそれぞれ使用して、このプロパティを取得または設定します。
  
アカウントの既定の配信ストアとしてストアを設定する場合の副作用の 1 つは、Outlook を開始すると、Outlook が存在しない場合、そのストアの検索フォルダーを作成し、To-Do バーにストアを一覧表示する場合です。
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)
- [定数 (アカウント管理 API)](constants-account-management-api.md)

