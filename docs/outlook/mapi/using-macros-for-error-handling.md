---
title: エラー処理のためのマクロを使用してください。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c4e216f2204f4ee97d9eeac81f77ce6a82fff3f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804199"
---
# <a name="using-macros-for-error-handling"></a>エラー処理のためのマクロを使用してください。

  
  
**適用されます**: Outlook 
  
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
   

