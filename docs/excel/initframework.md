---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- initframework function [excel 2007]
ms.localizationpriority: medium
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 932d1a42c104b364d6f6d584e4e8848469405688
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621431"
---
# <a name="initframework"></a>InitFramework

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
フレームワーク ライブラリを初期化するフレームワーク ライブラリ関数。これは単に、既に割り当てられているメモリを解放して、一時 **XLOPER**/ **XLOPER12** のメモリ データ構造を初期化します。 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a>パラメーター

この関数に引数はありません。
  
## <a name="return-value"></a>戻り値

この関数は値を返しません。
  
## <a name="example"></a>例

この例では **InitFramework** 関数を使用して、すべての一時メモリを解放します。 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a>関連項目



[フレームワーク ライブラリの関数](functions-in-the-framework-library.md)

