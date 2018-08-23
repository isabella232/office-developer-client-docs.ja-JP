---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: アカウントが Exchange アカウントの場合は true。
ms.openlocfilehash: db9f5ae46096d221ac3636a44f588c6a90ce146e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799553"
---
# <a name="propacctisexch"></a>PROP_ACCT_IS_EXCH

アカウントが Exchange アカウントの場合は true。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x0014  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|プロパティ タグ。  <br/> |0x00140003  <br/> |
|アクセス:  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

[IOlkAccount::GetProp](iolkaccount-getprop.md)を使用してこのプロパティを取得します。 クライアントがこのプロパティを設定しようとすると、このプロパティは**E_OLK_PROP_READ_ONLY**を返します。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)

