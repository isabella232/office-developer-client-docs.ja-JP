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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: baa2ac2e859b42234fcb07dd2bf521424ef9b465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804035"
---
# <a name="stnefproblemarray"></a>STnefProblemArray

  
  
**適用対象**: Outlook 
  
エンコード中に発生した問題を処理する 1 つまたは複数、またはトランスポート ニュートラル カプセル化形式 (TNEF) ストリームのデコードを記述する**STnefProblem**構造体の配列が含まれています。 
  
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

## <a name="members"></a>Members

 **cProblem**
  
> **かかわる問題**のメンバーで指定された配列内の要素の数。 
    
 **かかわる問題**
  
> [STnefProblem](stnefproblem.md)構造体の配列です。 各構造体には、プロパティまたは属性の問題の処理に関する情報が含まれています。 
    
## <a name="remarks"></a>注釈

[ITnef::ExtractProps](itnef-extractprops.md)メソッドと[ITnef::Finish](itnef-finish.md)メソッドの出力パラメーターが、構造体の**STnefProblemArray**と**ExtractProps へのポインターを受信する属性またはプロパティの処理中に問題が発生した場合****終了**各 MAPI_W_ERRORS_RETURNED の値を返すとします。 このエラー値は、処理中に問題が発生したし、 **STnefProblemArray**構造体が生成されたことを示します。 
  
**STnefProblem**構造体は、属性またはプロパティの処理中に生成されていない場合場合は、クライアント アプリケーションがその属性またはプロパティの処理が成功したことがあると仮定して続行できます。 唯一の例外は、ブロックをカプセル化のデコード中に問題が発生したときに発生します。 このデコード中にエラーが発生した場合は、構造体に[SCODE](scode.md)として MAPI_E_UNABLE_TO_COMPLETE が返されます。 この例では、ブロックに対応するコンポーネントのデコードを停止して、別のコンポーネントが続きますをデコードすること。 
  
## <a name="see-also"></a>関連項目



[STnefProblem](stnefproblem.md)
  
[SCODE](scode.md)


[MAPI の構造](mapi-structures.md)

