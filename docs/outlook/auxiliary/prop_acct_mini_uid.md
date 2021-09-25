---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: ユーザー プロファイル全体で一意のアカウントOutlookします。
ms.openlocfilehash: bcfede8ad2716bd09ec1abd3420b7e61777f4a0a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625631"
---
# <a name="prop_acct_mini_uid"></a>PROP_ACCT_MINI_UID

ユーザー プロファイル全体で一意のアカウントOutlookします。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccount」を参照してください](iolkaccount.md)。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x0003  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|プロパティ タグ:  <br/> |0x00030003  <br/> |
|アクセス:  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

[IOlkAccount::GetProp を使用してこのプロパティを取得します](iolkaccount-getprop.md)。 クライアントがこのプロパティを設定しようとすると、このプロパティは次 **E_OLK_PROP_READ_ONLY。** 
  
このプロパティは [、PROP_ACCT_ID](prop_acct_id.md) とは異なりますが、その値はアカウントが作成されたプロファイルの中と外側のアカウントを一意に識別しますが **、PROP_ACCT_ID** はアカウントが作成されたプロファイル内のすべてのアカウント間でのみ一意です。 これらのプロパティを持つメッセージが別の Outlook プロファイルと異なるアカウント セットを持つ 2 番目のコンピューターにローミングすると **、PROP_ACCT_MINI_UID** は元のプロファイルの元のアカウントを一意に識別できます。 ただし **、PROP_ACCT_ID** コンピューターのプロファイル内のアカウントと競合する可能性があります。 
  
## <a name="see-also"></a>関連項目

- [PROP_ACCT_ID](prop_acct_id.md)  
- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)

