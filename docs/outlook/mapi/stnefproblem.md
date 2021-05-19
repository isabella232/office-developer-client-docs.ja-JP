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
  
トランスポート ニュートラル カプセル化形式 (TNEF) ストリームのエンコードまたはデコード中に発生したプロパティまたは属性処理の問題に関する情報が含まれます。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Tnef.h  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a>Members

 **ulComponent**
  
> 問題が発生した処理の種類。 メッセージ処理中に問題が発生した場合 **、ulComponent** メンバーは 0 に設定されます。 添付ファイルの処理中に問題が発生した場合 **、ulComponent** は対応する添付ファイルの値 **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) PR_ATTACH_NUMに設定されます。
    
 **ulAttribute**
  
> **ulPropTag** メンバーによって示されるプロパティに関連付けられた属性、またはカプセル化ブロックをデコードするときに TNEF 処理の問題が発生した場合、次のいずれかの値を指定します。 
    
 _attMAPIProps_
  
> メッセージ レベル
    
 _attAttachment_
  
> 添付ファイルのレベル
    
 **ulPropTag**
  
> カプセル化ブロックをデコードするときに問題が発生した場合を除き、TNEF 処理の問題を引き起こしたプロパティのプロパティ タグ 。その場合 **、ulPropTag** は 0 に設定されます。 
    
 **scode**
  
> 処理中に発生した問題を示すエラー値。
    
## <a name="remarks"></a>注釈

属性またはプロパティの処理中に **STnefProblem** 構造体が生成されない場合、アプリケーションは、その属性またはプロパティの処理が成功したという前提で続行できます。 カプセル化ブロックのデコード中に問題が発生した場合、唯一の例外が発生します。 この場合、ブロックに対応するコンポーネントのデコードが停止され、別のコンポーネントでデコードが継続されます。 
  
## <a name="see-also"></a>関連項目



[STnefProblemArray](stnefproblemarray.md)
  
[PidTagAttachNumber 標準プロパティ](pidtagattachnumber-canonical-property.md)


[MAPI の構造](mapi-structures.md)

