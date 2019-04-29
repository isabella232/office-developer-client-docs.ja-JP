---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: アカウントスタンプを返します。
ms.openlocfilehash: fe3c6e65e12ab62bd1c2ec0245e4a22502f610eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408251"
---
# <a name="propacctstamp"></a>PROP_ACCT_STAMP

アカウントスタンプを返します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x000d  <br/> |
|プロパティの種類:  <br/> |PT_UNICODE  <br/> |
|プロパティタグ:  <br/> |0x000d001f  <br/> |
|接続  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

[IOlkAccount:: getprop](iolkaccount-getprop.md)を使用して、このプロパティを取得します。 クライアントがこのプロパティを設定しようとすると、このプロパティは**E_OLK_PROP_READ_ONLY**を返します。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)  
- [定数 (アカウント管理 API)](constants-account-management-api.md)

