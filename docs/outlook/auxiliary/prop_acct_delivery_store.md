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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327672"
---
# <a name="propacctdeliverystore"></a>PROP_ACCT_DELIVERY_STORE

アカウントの既定の配信ストアのエントリ ID を表します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x0018  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|プロパティタグ:  <br/> |0x00180102  <br/> |
|接続  <br/> |読み取り/書き込み  <br/> |
   
## <a name="remarks"></a>解説

[IOlkAccount:: getprop](iolkaccount-getprop.md)または[IOlkAccount:: setprop](iolkaccount-setprop.md)を使用して、このプロパティを取得または設定します。
  
アカウントの既定の配信ストアとしてストアを設定する場合の副次的な影響の1つは、outlook を起動したときに、そのストアの検索フォルダーがまだ存在しない場合はそのストアの検索フォルダーを作成し、そのストアを To do バーに表示することです。
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)
- [定数 (アカウント管理 API)](constants-account-management-api.md)

