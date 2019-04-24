---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Outlook プロファイル全体で一意のアカウント識別子を返します。
ms.openlocfilehash: 209f7dd89b8d947b999f2a068373aaf61a3e9784
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327630"
---
# <a name="propacctminiuid"></a>PROP_ACCT_MINI_UID

Outlook プロファイル全体で一意のアカウント識別子を返します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x0003  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|プロパティタグ:  <br/> |0x0003000 3  <br/> |
|接続  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>解説

[IOlkAccount:: getprop](iolkaccount-getprop.md)を使用して、このプロパティを取得します。 クライアントがこのプロパティを設定しようとすると、このプロパティは**E_OLK_PROP_READ_ONLY**を返します。 
  
このプロパティの値は、アカウントが作成されたプロファイルの内部と外部のアカウントを一意に識別するという点で[PROP_ACCT_ID](prop_acct_id.md)とは異なりますが、 **PROP_ACCT_ID**はその1つのプロファイル内のすべてのアカウント間でのみ一意です。アカウントが作成された。 これらのプロパティを持つメッセージが、異なる Outlook プロファイルおよび異なるアカウントのセットを持つ2番目のコンピューターに移動すると、 **PROP_ACCT_MINI_UID**は元のプロファイルで元のアカウントを一意に識別できます。 ただし、 **PROP_ACCT_ID**は、2番目のコンピューターのプロファイルのアカウントと競合する可能性があります。 
  
## <a name="see-also"></a>関連項目

- [PROP_ACCT_ID](prop_acct_id.md)  
- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)

