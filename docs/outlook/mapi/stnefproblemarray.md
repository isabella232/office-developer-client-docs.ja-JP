---
title: STnefProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.STnefProblemArray
api_type:
- COM
ms.assetid: 115d845b-4168-4d49-b880-219ee28baa9a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d15fca75372aa8fea074e5259506ddb6acf40c2f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591053"
---
# <a name="stnefproblemarray"></a>STnefProblemArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート ニュートラル カプセル化形式 (TNEF) ストリームのエンコードまたはデコード中に発生した 1 つ以上の処理の問題を説明する **STnefProblem** 構造体の配列を格納します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Tnef.h  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a>メンバー

 **cProblem**
  
> aProblem メンバーで指定された配列 **内の要素の** 数。 
    
 **aProblem**
  
> [STnefProblem 構造体の](stnefproblem.md)配列。 各構造には、プロパティまたは属性処理の問題に関する情報が含まれる。 
    
## <a name="remarks"></a>注釈

属性またはプロパティの処理中に問題が発生した場合 [、ITnef::ExtractProps](itnef-extractprops.md) メソッドと [ITnef::Finish](itnef-finish.md) メソッドの出力パラメーターは、それぞれ **STnefProblemArray** 構造体へのポインターを受け取り **、ExtractProps** and **Finish** は値 MAPI_W_ERRORS_RETURNED を返します。 このエラー値は、処理中に問題が発生し **、STnefProblemArray 構造が生成されたかどうかを** 示します。 
  
属性またはプロパティの処理中に **STnefProblem** 構造体が生成されない場合、クライアント アプリケーションは、その属性またはプロパティの処理が成功したという前提で続行できます。 カプセル化ブロックのデコード中に問題が発生した場合、唯一の例外が発生します。 このデコード中にエラーが発生した場合、MAPI_E_UNABLE_TO_COMPLETEで [SCODE として](scode.md) 返されます。 この場合、ブロックに対応するコンポーネントのデコードが停止され、別のコンポーネントでデコードが継続されます。 
  
## <a name="see-also"></a>関連項目



[STnefProblem](stnefproblem.md)
  
[SCODE](scode.md)


[MAPI の構造](mapi-structures.md)

