---
title: ITnefFinishComponent
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.FinishComponent
api_type:
- COM
ms.assetid: bcdd0688-0897-47d7-9601-f592ba453b39
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0242015680f11e5be6ae8ea9987e5778dc7cdf05
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594363"
---
# <a name="itneffinishcomponent"></a>ITnef::FinishComponent

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
トランスポート ニュートラル カプセル化形式 (TNEF) ストリームに同時に 1 つのメッセージからの個々 のコンポーネントを処理します。
  
```cpp
HRESULT FinishComponent(
  ULONG ulFlags,
  ULONG ulComponentID,
  LPSPropTagArray lpCustomPropList,
  LPSPropValue lpCustomProps,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]どのコンポーネントが完了するかを制御するフラグのビットマスクです。 いずれか、または次のフラグの一方を設定する必要があります。
    
TNEF_COMPONENT_ATTACHMENT 
  
> 添付ファイル オブジェクトの処理を完了します。_ulComponentID_パラメーターには、添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) のプロパティが含まれています。 
    
TNEF_COMPONENT_MESSAGE 
  
> メッセージ オブジェクトの処理を完了します。 
    
 _ulComponentID_
  
> [in] メッセージ、または添付ファイルの**PR_ATTACH_NUM**プロパティを処理するための処理を示すために 0 を返します。 _UlFlags_パラメーターに TNEF_COMPONENT_MESSAGE フラグを設定すると、 _ulComponentID_は 0 にする必要があります。 
    
 _lpCustomPropList_
  
> [in]_LpCustomProps_パラメーターで渡されたプロパティを識別するプロパティ タグを含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 _LpCustomProps_の各プロパティの値と、 _lpCustomPropList_パラメーター内のプロパティ タグの間の 1 対 1 の対応をする必要があります。 
    
 _lpCustomProps_
  
> [in]エンコードするためにプロパティのプロパティ値を含む[SPropValue](spropvalue.md)構造体へのポインター。 
    
 _lpPropList_
  
> [in]エンコードするにはプロパティのプロパティ タグを含む**SPropTagArray**構造体へのポインター。 
    
 _lppProblems_
  
> [out]返された[STnefProblemArray](stnefproblemarray.md)構造体へのポインターへのポインター。 **STnefProblemArray**構造体は、どのプロパティでは、存在する場合、されたエンコードされません正しくを示します。 _LppProblems_パラメーターに NULL を渡した場合、プロパティの問題の配列は返されません。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

プロバイダー、メッセージ ストア プロバイダー、および_ulFlags_パラメーターで設定するフラグで示されるように、TNEF は、メッセージまたは添付ファイルのいずれか 1 つのコンポーネントの処理を実行するのにはゲートウェイの呼び出し、 **ITnef::FinishComponent**メソッドを転送します。 
  
有効にするコンポーネントで処理するため、呼び出し元のプロバイダーまたはゲートウェイはエンコードを受け取るオブジェクトを開く、 [OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の_ulFlags_で TNEF_COMPONENT_ENCODING フラグを渡します。 
  
_LpCustomPropList_および_lpCustomProps_パラメーターに値を渡すことは、コンポーネントの[ITnef::SetProps](itnef-setprops.md)メソッドによって実行されるのと同じエンコーディングを実行します。 _UlFlags_で設定 TNEF_PROP_INCLUDE フラグを使用して、 [ITnef::AddProps](itnef-addprops.md)メソッドによって実行されるコンポーネントのエンコードと同じを実行する_lpPropList_パラメーターに値を渡すことです。 これらの値を渡すことを使用すると、複数の呼び出しではなく単一の呼び出しを使用してエンコードを実行します。
  
TNEF の実装では、 **FinishComponent**プロセスを停止することがなく TNEF ストリームのエンコーディングの問題を報告します。 _LppProblems_で返された**STnefProblemArray**構造体は、どの TNEF 属性または MAPI プロパティでは、存在する場合、処理できませんでしたを示します。 **STnefProblemArray**に含まれている**STnefProblem**の構造体のいずれかの**scode**メンバーの戻り値は、特定の問題を示します。 プロバイダーまたはゲートウェイは、すべてのプロパティまたは属性の**FinishComponent**が、問題レポートを返さないが正常に処理されたことを前提として処理できます。 
  
_LppProblems_; で NULL を渡すことができます問題の配列を持つプロバイダーまたはゲートウェイが機能しない場合この例では、問題の配列は返されません。
  
_LppProblems_で返される値は、呼び出しが S_OK を返す場合にのみ有効です。 S_OK が返されると、プロバイダーまたはゲートウェイは[STnefProblemArray](stnefproblemarray.md)構造体で返される値を確認する必要があります。 呼び出しでエラーが発生した場合、 **STnefProblemArray**構造体が入っていませんと、プロバイダーまたはゲートウェイが呼び出し元する必要があります使用または構造体を解放します。 呼び出しでエラーが発生しなかった場合、呼び出し元のプロバイダーまたはゲートウェイ必要がありますメモリを解放**STnefProblemArray**の[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって。 
  
## <a name="see-also"></a>関連項目



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[SPropTagArray](sproptagarray.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

