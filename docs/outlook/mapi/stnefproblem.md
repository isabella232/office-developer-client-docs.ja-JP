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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8595cdb411e68f2aed3ac063b2b81965e9b4d975
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804024"
---
# <a name="stnefproblem"></a>STnefProblem

  
  
**適用対象**: Outlook 
  
エンコードまたはトランスポート ニュートラル カプセル化形式 (TNEF) ストリームのデコード中に発生するプロパティまたは属性の処理の問題についての情報が含まれています。
  
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
  
> 問題が発生した処理の種類です。 メッセージの処理中に問題が発生した場合は、 **ulComponent**メンバーが 0 に設定されます。 添付ファイルの処理中に問題が発生した場合、 **ulComponent**は対応する添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) の値に設定されています。
    
 **ulAttribute**
  
> プロパティに関連付けられている属性は、 **ulPropTag**のメンバー、または、TNEF の処理の問題が発生したときとカプセル化をデコードすることをブロックする、次のいずれかの示されています。 
    
 _attMAPIProps_
  
> メッセージのレベル
    
 _attAttachment_
  
> 添付ファイルのレベル
    
 **ulPropTag**
  
> ケース**ulPropTag**が 0 に設定されている、カプセル化、ブロックをデコードするときに問題が発生する場合を除き、TNEF 処理の問題の原因となったプロパティのプロパティ タグです。 
    
 **scode**
  
> エラーの処理中に発生した問題を示す値。
    
## <a name="remarks"></a>注釈

**STnefProblem**構造体は、属性またはプロパティの処理中に生成されていない場合場合は、アプリケーションがその属性またはプロパティの処理が成功したことを前提として続けることができます。 唯一の例外は、ブロックをカプセル化のデコード中に問題が発生したときに発生します。 この例では、ブロックに対応するコンポーネントのデコードを停止して、別のコンポーネントが続きますをデコードすること。 
  
## <a name="see-also"></a>関連項目



[STnefProblemArray](stnefproblemarray.md)
  
[PidTagAttachNumber 標準プロパティ](pidtagattachnumber-canonical-property.md)


[MAPI の構造](mapi-structures.md)

