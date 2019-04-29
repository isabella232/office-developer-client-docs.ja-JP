---
title: STnefProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblem
api_type:
- COM
ms.assetid: 3fe651b7-0ddf-42fd-8277-9224505be1a8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 19d20a3fb06f6a0a0671ba4bfd938da314001778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435181"
---
# <a name="stnefproblem"></a>STnefProblem

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポートニュートラルカプセル化形式 (TNEF) ストリームのエンコードまたはデコード中に発生したプロパティまたは属性処理の問題に関する情報が含まれています。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Tnef  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a>メンバー

 **ulcomponent**
  
> 問題が発生した処理の種類。 メッセージ処理中に問題が発生した場合、 **ulcomponent**メンバーは0に設定されます。 添付ファイルの処理中に問題が発生した場合、 **ulcomponent**は対応する添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) 値に設定されます。
    
 **ulattribute**
  
> 属性。 **ulPropTag**メンバーによって示されるプロパティに関連付けられている属性。または、カプセル化ブロックのデコード時に TNEF 処理の問題が発生した場合は、次のいずれかの値になります。 
    
 _attMAPIProps_
  
> メッセージレベル
    
 _添付ファイル_
  
> 添付ファイルレベル
    
 **ulPropTag**
  
> **ulPropTag**が0に設定されている場合を除き、TNEF 処理の問題の原因となったプロパティのプロパティタグ。 
    
 **scode as scode**
  
> 処理中に発生した問題を示すエラー値。
    
## <a name="remarks"></a>注釈

属性またはプロパティの処理中に**STnefProblem**構造体が生成されない場合、アプリケーションは、その属性またはプロパティの処理が正常に終了したことを前提として続行できます。 唯一の例外は、カプセル化ブロックのデコード中に問題が発生した場合です。 この場合、ブロックに対応するコンポーネントのデコードが停止され、別のコンポーネントでデコードが続行されます。 
  
## <a name="see-also"></a>関連項目



[STnefProblemArray](stnefproblemarray.md)
  
[PidTagAttachNumber 標準プロパティ](pidtagattachnumber-canonical-property.md)


[MAPI の構造](mapi-structures.md)

