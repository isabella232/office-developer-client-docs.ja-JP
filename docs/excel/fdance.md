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
ms.openlocfilehash: b7a2fbdf723d06dcf9b02789178d7d12d0515884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798883"
---
# <a name="fdance"></a>fDance

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
ユーザーが** [Esc]** を押すまで、作業中のワークシートの選択セルを変更するサンプル ユーザー定義コマンド。GENERIC.xll が読み込まれると、このコマンドにアクセスするためのユーザー定義メニュー [Generic] を作成します。
  
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

