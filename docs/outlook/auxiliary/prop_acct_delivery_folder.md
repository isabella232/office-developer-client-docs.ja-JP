---
title: PROP_ACCT_DELIVERY_FOLDER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a409c49b-b390-021e-2ec1-7a5932a0c8de
description: アカウントの既定の配信フォルダーのエントリ ID を表します。
ms.openlocfilehash: 1bac4890791edfe661599d383e2cb048bf4c42fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327700"
---
# <a name="propacctdeliveryfolder"></a>PROP_ACCT_DELIVERY_FOLDER

アカウントの既定の配信フォルダーのエントリ ID を表します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x0019  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|プロパティタグ:  <br/> |0x00190102  <br/> |
|接続  <br/> |読み取り/書き込み  <br/> |
   
## <a name="remarks"></a>解説

[IOlkAccount:: getprop](iolkaccount-getprop.md)または[IOlkAccount:: setprop](iolkaccount-setprop.md)を使用して、このプロパティを取得または設定します。
  
既定の配信フォルダーは**受信トレイ**です。
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)  
- [定数 (アカウント管理 API)](constants-account-management-api.md)

