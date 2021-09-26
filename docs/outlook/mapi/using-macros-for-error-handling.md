---
title: エラー処理にマクロを使用する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0d3c10a167c961dd2dfe8e31313f6b0f5d827abe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619499"
---
# <a name="using-macros-for-error-handling"></a>エラー処理にマクロを使用する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
HRESULT 値の操作を容易にするマクロがいくつかあります。
  
エラーまたは成功をテストするマクロのセットは、HR_SUCCEEDEDとHR_FAILED FAILED です。 SUCCEEDED は、システムと同HR_SUCCEEDED FAILED は、同じHR_FAILED。
  
この場合 **、ResultFromScode** マクロを使用して、HRESULT 変数に対応する HRESULT 値を設定S_OK。 
  
一般的に使用されるマクロについては、次の表で簡単に説明します。
  
|**Macro**|**説明**|
|:-----|:-----|
|**MAKE_HRESULT** <br/> |コンポーネントから HRESULT を作成します。  <br/> |
|**HR_SUCCEEDED** <br/> |成功または警告の条件について HRESULT をテストします。  <br/> |
|**HR_FAILED** <br/> |エラー状態の HRESULT をテストします。  <br/> |
|**HRESULT_CODE** <br/> |HRESULT のエラー コード部分を抽出します。  <br/> |
|**HRESULT_FACILITY** <br/> |HRESULT から施設を抽出します。  <br/> |
|**HRESULT_SEVERITY** <br/> |重大度ビットを重大度から抽出します。  <br/> |
|**成功しました** <br/> |成功または警告の条件について HRESULT をテストします。  <br/> |
|**FAILED** <br/> |エラー状態の HRESULT をテストします。  <br/> |
   

