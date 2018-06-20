---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: アカウントの既定の配信ストアのエントリ ID を表します。
ms.openlocfilehash: 72c5325e70a6e8b42ee433d8d674c2b2ea0c8398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799556"
---
# <a name="propacctdeliverystore"></a>PROP_ACCT_DELIVERY_STORE

アカウントの既定の配信ストアのエントリ ID を表します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x0018  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|プロパティ タグ。  <br/> |0x00180102  <br/> |
|アクセス:  <br/> |値の取得および設定が可能です。  <br/> |
   
## <a name="remarks"></a>備考

取得または[IOlkAccount::GetProp](iolkaccount-getprop.md)または[IOlkAccount::SetProp](iolkaccount-setprop.md)をそれぞれ使用して、このプロパティを設定します。
  
アカウントの既定の配信ストアとして設定して、店舗の副作用の 1 つは Outlook を起動するとき Outlook が作成されるそのストアの検索フォルダーが存在し、to do バーのストアを一覧表示する操作を行いますがされていない場合。
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)
- [定数 (アカウント管理 API)](constants-account-management-api.md)

