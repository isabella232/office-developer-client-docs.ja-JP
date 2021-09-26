---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: True の場合は、アカウントがアカウントExchangeします。
ms.openlocfilehash: 67562acbb7ee5c29948d9e2dd7bfdbf9a7623135
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631168"
---
# <a name="prop_acct_is_exch"></a>PROP_ACCT_IS_EXCH

True の場合は、アカウントがアカウントExchangeします。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccount」を参照してください](iolkaccount.md)。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x0014  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|プロパティ タグ:  <br/> |0x00140003  <br/> |
|アクセス:  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

[IOlkAccount::GetProp を使用してこのプロパティを取得します](iolkaccount-getprop.md)。 クライアントがこのプロパティを設定しようとすると、このプロパティは次 **E_OLK_PROP_READ_ONLY。** 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)

