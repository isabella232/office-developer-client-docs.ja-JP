---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- fdance function [excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a191c07d2a06a1cb6123c235e8fac69d90426758
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409049"
---
# <a name="fdance"></a>fDance

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
ユーザーが **[Esc]** を押すまで、作業中のワークシートの選択セルを変更するサンプル ユーザー定義コマンド。GENERIC.xll が読み込まれると、このコマンドにアクセスするためのユーザー定義メニュー [Generic] を作成します。
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a>パラメーター

この関数にはパラメーターはありません。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

この関数は、常に 1 を返します。
  
## <a name="remarks"></a>注釈

これは、時間のかかる操作の例です。関数 [xlAbort](xlabort.md) を呼び出すこともあります。これは (協調的マルチタスキングを支援する) プロセッサを生成し、ユーザーが **[Esc]** を押して操作を取り消したかどうかを確認します。ボタンが押された場合は、ユーザーが中止操作をキャンセルできるようにします。 
  
### <a name="example"></a>例

この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。 
  
## <a name="see-also"></a>関連項目



[汎用 DLL の関数](functions-in-the-generic-dll.md)

