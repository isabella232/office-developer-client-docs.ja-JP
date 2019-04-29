---
title: エラー処理にマクロを使用する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9e6901d6583e7a7924a4a7c19c0a262bcef74bd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435566"
---
# <a name="using-macros-for-error-handling"></a>エラー処理にマクロを使用する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
HRESULT 値を使用して操作しやすくするために、いくつかのマクロが用意されています。
  
失敗または成功をテストするマクロは、HR_SUCCEEDED と HR_FAILED の2つのセットがあり、成功して失敗しました。 SUCCEEDED は HR_SUCCEEDED と同じで、FAILED は HR_FAILED と同じです。
  
この場合は、 **resultfromscode**マクロを使用して、hresult 変数を S_OK の対応する hresult 値に設定します。 
  
一般的に使用されるマクロについては、次の表で簡単に説明します。
  
|**Macro**|**説明**|
|:-----|:-----|
|**MAKE_HRESULT** <br/> |コンポーネントから HRESULT を構築します。  <br/> |
|**HR_SUCCEEDED** <br/> |成功または警告状態の HRESULT をテストします。  <br/> |
|**HR_FAILED** <br/> |エラー状態の HRESULT をテストします。  <br/> |
|**HRESULT_CODE** <br/> |HRESULT のエラーコード部分を抽出します。  <br/> |
|**HRESULT_FACILITY** <br/> |HRESULT からファシリティを抽出します。  <br/> |
|**HRESULT_SEVERITY** <br/> |重要度から重要度ビットを抽出します。  <br/> |
|**失敗** <br/> |成功または警告状態の HRESULT をテストします。  <br/> |
|**フェール** <br/> |エラー状態の HRESULT をテストします。  <br/> |
   

