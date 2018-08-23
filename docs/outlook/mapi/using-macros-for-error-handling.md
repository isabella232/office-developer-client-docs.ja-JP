---
title: エラー処理のためのマクロの使用
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 715cd001c5eab89f40c31200a12deaf6981b9a61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567126"
---
# <a name="using-macros-for-error-handling"></a>エラー処理のためのマクロの使用

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
HRESULT 値を操作するが容易にいくつかのマクロがあります。
  
失敗または成功をテストするマクロの 2 つのセットが生成されます: HR_SUCCEEDED と HR_FAILED と成功と失敗します。 成功しました、HR_SUCCEEDED と失敗と同じ HR_FAILED と同じです。
  
この場合は、S_OK の対応する HRESULT 値を HRESULT の変数を設定するのには、 **ResultFromScode**マクロを使用します。 
  
一般的に使用されるマクロは次の表に簡単に説明します。
  
|**マクロ**|**説明**|
|:-----|:-----|
|**MAKE_HRESULT** <br/> |HRESULT のコンポーネントからを構築します。  <br/> |
|**HR_SUCCEEDED** <br/> |成功または警告状態の HRESULT をテストします。  <br/> |
|**HR_FAILED** <br/> |エラーの HRESULT をテストします。  <br/> |
|**HRESULT_CODE** <br/> |HRESULT のエラー コードの一部を抽出します。  <br/> |
|**HRESULT_FACILITY** <br/> |HRESULT から施設を抽出します。  <br/> |
|**HRESULT_SEVERITY** <br/> |重大度の重大度のビットを抽出します。  <br/> |
|**成功しました** <br/> |成功または警告状態の HRESULT をテストします。  <br/> |
|**失敗しました。** <br/> |エラーの HRESULT をテストします。  <br/> |
   

