---
title: ITnefExtractProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.ExtractProps
api_type:
- COM
ms.assetid: 9169a5be-21dd-4938-8db3-522bea165c92
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 26949f10e22c4d2ea49594ee3365ae7d3bb3662d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801247"
---
# <a name="itnefextractprops"></a>ITnef::ExtractProps

  
  
**適用対象**: Outlook 
  
TNEF のカプセル化のプロパティを抽出します。 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]プロパティをデコードする方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
TNEF_PROP_EXCLUDE 
  
> _LpPropList_パラメーターで指定されていないすべてのプロパティをデコードします。 
    
TNEF_PROP_INCLUDE 
  
> _LpPropList_で指定されたすべてのプロパティをデコードします。
    
 _lpPropList_
  
> [in]含めるか、デコード処理から除外するプロパティの一覧へのポインター。
    
 _lpProblems_
  
> [out]返された[STnefProblemArray](stnefproblemarray.md)構造体へのポインターへのポインター。 **STnefProblemArray**構造体は、どのプロパティでは、存在する場合、されたエンコードされません正しくを示します。 _LpProblems_パラメーターに NULL を渡した場合、プロパティの問題の配列は返されません。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値または値が返されます。
    
MAPI_E_CORRUPT_DATA 
  
> ストリームにデコードされたデータが壊れています。
    
## <a name="remarks"></a>注釈

トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイ メソッドを呼び出す**ITnef::ExtractProps**を抽出する (これをデコード) は、プロパティをメッセージまたは[OpenTnefStream](opentnefstream.md)関数に渡された添付ファイルをカプセル化します。 呼び出し元のプロバイダーまたはゲートウェイには、デコードするためのプロパティの一覧を指定できます。 プロバイダーとゲートウェイも使用できます**ExtractProps**の添付ファイルに対して特別な処理情報を提供します。 
  
 **ExtractProps**には、デコードされたプロパティを使用して、 **OpenTnefStream**に渡された元のメッセージが表示されます。 **ExtractProps**の後続の呼び出しはメッセージに戻るし、プロパティの新しいリストを抽出します。 
  
キューにアクションが要求されるは、 **ITnef::Finish**メソッドが呼び出されるまで、 [ITnef::AddProps](itnef-addprops.md)メソッドとは異なり、 **ExtractProps**メソッドは、呼び出されたときにすぐにカプセル化されたプロパティをデコードします。 そのため、移行先のメッセージのカプセル化をデコードすることが比較的空でなければなりません。 カプセル化されたプロパティでは、移行先のメッセージ内の既存のプロパティが上書きされます。 
  
 **ExtractProps**は、 **OpenTnefStream**または[OpenTnefStreamEx](opentnefstreamex.md)関数の場合、TNEF_DECODE フラグを使用して開かれているオブジェクトでのみサポートされます。 
  
TNEF の実装では、 **ExtractProps**プロセスを停止することがなく TNEF ストリームのエンコーディングの問題を報告します。 _LpProblems_で返された[STnefProblemArray](stnefproblemarray.md)構造体は、どの TNEF 属性または MAPI プロパティでは、存在する場合、処理できませんでしたを示します。 **STnefProblemArray**に含まれている**STnefProblem**の構造体のいずれかの**scode**メンバーの戻り値は、特定の問題を示します。 プロバイダーまたはゲートウェイは、すべてのプロパティまたは属性の**ExtractProps**が、問題レポートを返さないが正常に処理されたことを前提として処理できます。 
  
> [!NOTE]
> MAPI のカプセル化のブロック内のプロパティを処理できません、TNEF ストリームのデコード時に、ストリームの信頼性が低いままのカプセル化のブロックをデコードすることを停止して、問題が報告されました。 この種の問題の問題の配列には、 **ulPropTag**メンバーの 0 L が含まれています`attMAPIProps`または`attAttachment` **ulAttribute**のメンバー、および**scode**メンバーの MAPI_E_UNABLE_TO_COMPLETE のです。 MAPI のカプセル化のブロックのデコードだけ、ストリームのデコードではないメモが停止しました。 ストリームのデコードは、次の属性ブロックを続行します。 
  
_LppProblems_; で NULL を渡すことができます問題の配列を持つプロバイダーまたはゲートウェイが機能しない場合この例では、問題の配列は返されません。 
  
_LpProblems_で返される値は、呼び出しが S_OK を返す場合にのみ有効です。 S_OK が返されると、プロバイダーまたはゲートウェイは**STnefProblemArray**構造体で返される値を確認する必要があります。 呼び出しでエラーが発生した場合**STnefProblemArray**構造体が記入されていませんし、プロバイダーまたはゲートウェイが呼び出し元する必要があります使用または構造体を解放します。 呼び出しでエラーが発生しなかった場合、呼び出し元のプロバイダーまたはゲートウェイ必要があります[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって**STnefProblemArray**構造体のメモリを解放します。 
  
## <a name="see-also"></a>関連項目



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::Finish](itnef-finish.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

