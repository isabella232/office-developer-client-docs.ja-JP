---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: accountsendstamp を返します。
ms.openlocfilehash: d860a117e4ab5470f84ff1807cb6246cd852d24b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327609"
---
# <a name="propacctsendstamp"></a>PROP_ACCT_SEND_STAMP

アカウント "send" スタンプを返します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x000e  <br/> |
|プロパティの種類:  <br/> |PT_UNICODE  <br/> |
|プロパティタグ:  <br/> |0x000e001f  <br/> |
|接続  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>解説

[IOlkAccount:: getprop](iolkaccount-getprop.md)を使用して、このプロパティを取得します。 クライアントがこのプロパティを設定しようとすると、このプロパティは**E_OLK_PROP_READ_ONLY**を返します。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)  
- [定数 (アカウント管理 API)](constants-account-management-api.md)

