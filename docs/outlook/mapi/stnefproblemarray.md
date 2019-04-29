---
title: STnefProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblemArray
api_type:
- COM
ms.assetid: 115d845b-4168-4d49-b880-219ee28baa9a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 721b14f101e87299f654507f94d4a957f905cac1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434264"
---
# <a name="stnefproblemarray"></a>STnefProblemArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポートニュートラルカプセル化形式 (TNEF) ストリームのエンコードまたはデコード中に発生した1つ以上の処理上の問題について説明する**STnefProblem**構造体の配列が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Tnef  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a>メンバー

 **cproblem**
  
> **aproblem**メンバーで指定されている配列内の要素の数。 
    
 **aproblem**
  
> [STnefProblem](stnefproblem.md)構造体の配列。 各構造体には、プロパティまたは属性処理の問題に関する情報が含まれています。 
    
## <a name="remarks"></a>注釈

属性またはプロパティの処理中に問題が発生した場合、 [ITnef:: ExtractProps](itnef-extractprops.md)メソッドと[ITnef:: Finish](itnef-finish.md)メソッドの出力パラメーターは、それぞれ**STnefProblemArray**構造体へのポインターを受け取り、 **ExtractProps****完了**するたびに、MAPI_W_ERRORS_RETURNED 値を返します。 このエラー値は、処理中に問題が発生し、 **STnefProblemArray**構造が生成されたことを示します。 
  
属性またはプロパティの処理中に**STnefProblem**構造体が生成されない場合、クライアントアプリケーションは、その属性またはプロパティの処理が正常に終了したことを前提として続行できます。 唯一の例外は、カプセル化ブロックのデコード中に問題が発生した場合です。 このデコード中にエラーが発生した場合は、MAPI_E_UNABLE_TO_COMPLETE を構造内の[SCODE](scode.md)として返すことができます。 この場合、ブロックに対応するコンポーネントのデコードが停止され、別のコンポーネントでデコードが続行されます。 
  
## <a name="see-also"></a>関連項目



[STnefProblem](stnefproblem.md)
  
[SCODE](scode.md)


[MAPI の構造](mapi-structures.md)

