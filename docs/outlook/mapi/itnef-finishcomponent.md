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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c8dc10bdb8bcde15dccf7bab4d9e10d2481cef11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416441"
---
# <a name="itneffinishcomponent"></a>ITnef::FinishComponent

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの個々のコンポーネントを一度に 1 つ処理して、Transport-Neutralカプセル化形式 (TNEF) ストリームに処理します。
  
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

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]終了するコンポーネントを制御するフラグのビットマスク。 次のいずれかのフラグを設定する必要があります。
    
TNEF_COMPONENT_ATTACHMENT 
  
> 添付ファイル オブジェクトの処理が完了します。  _ulComponentID_ パラメーターには、添付 **ファイルPR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティが含まれる。 
    
TNEF_COMPONENT_MESSAGE 
  
> メッセージ オブジェクトの処理が完了します。 
    
 _ulComponentID_
  
> [in] 0 メッセージの処理を示す場合、 **または** PR_ATTACH_NUM添付ファイルのプロパティを指定します。 _ulFlags_ パラメーター TNEF_COMPONENT_MESSAGEフラグが設定されている場合 _、ulComponentID_ は 0 である必要があります。 
    
 _lpCustomPropList_
  
> [in]_lpCustomProps_ パラメーターで渡されるプロパティを識別するプロパティ タグを含む [SPropTagArray](sproptagarray.md)構造体へのポインター。 _lpCustomProps_ の各プロパティ値と _lpCustomPropList_ パラメーターのプロパティ タグの間には、1 対 1 の対応が必要です。 
    
 _lpCustomProps_
  
> [in]エンコードするプロパティのプロパティ値を含む [SPropValue](spropvalue.md) 構造体へのポインター。 
    
 _lpPropList_
  
> [in]エンコードするプロパティのプロパティ タグを含む **SPropTagArray** 構造体へのポインター。 
    
 _lppProblems_
  
> [out]返される [STnefProblemArray 構造体へのポインターを指すポインター](stnefproblemarray.md) 。 **STnefProblemArray** 構造体は、適切にエンコードされていないプロパティがある場合は、どのプロパティを示します。 _lppProblems_ パラメーターに NULL が渡された場合、プロパティの問題の配列は返されません。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

トランスポート プロバイダー、メッセージ ストア プロバイダー、ゲートウェイは **ITnef::FinishComponent** メソッドを呼び出して  _、ulFlags_ パラメーターで設定されたフラグで示されているメッセージまたは添付ファイルのどちらかの 1 つのコンポーネントに対して TNEF 処理を実行します。 
  
コンポーネント処理を有効にする場合、呼び出し元プロバイダーまたはゲートウェイは、エンコードを受け取るオブジェクトを開いた [OpenTnefStream](opentnefstream.md)または [OpenTnefStreamEx](opentnefstreamex.md)関数の _ulFlags_ で TNEF_COMPONENT_ENCODING フラグを渡します。 
  
_lpCustomPropList_ パラメーターと _lpCustomProps_ パラメーターで値を渡す場合 [、ITnef::SetProps](itnef-setprops.md)メソッドで行われるコンポーネント エンコードと同等のコンポーネント エンコードが実行されます。 _lpPropList_ パラメーターに値を渡す場合 _、ulFlags_ で TNEF_PROP_INCLUDE フラグが設定された [ITnef::AddProps](itnef-addprops.md)メソッドで行われるのと同等のコンポーネント エンコードが実行されます。 これらの値を渡すと、複数の呼び出しではなく、1 回の呼び出しでエンコードを実行できます。
  
TNEF 実装では **、FinishComponent** プロセスを停止せずに TNEF ストリーム エンコードの問題を報告します。 _lppProblems_ で返される **STnefProblemArray** 構造体は、処理できない TNEF 属性または MAPI プロパティを示します(指定されている場合)。 **STnefProblemArray** に含まれる **STnefProblem** 構造体の scode メンバーで返される値は、特定の問題を示します。  プロバイダーまたはゲートウェイは **、FinishComponent** が問題レポートを返さないすべてのプロパティまたは属性が正常に処理されたという前提で動作できます。 
  
プロバイダーまたはゲートウェイが問題の配列で動作しない場合は  _、lppProblems で NULL を渡す可能性があります_。この場合、問題のある配列は返されません。
  
_lppProblems_ で返される値は、呼び出しが無効な値を返すS_OK。 このS_OK返される場合、プロバイダーまたはゲートウェイは [、STnefProblemArray](stnefproblemarray.md) 構造体で返される値を確認する必要があります。 呼び出しでエラーが発生した場合 **、STnefProblemArray** 構造体は入力されないので、呼び出し元プロバイダーまたはゲートウェイは構造体を使用または解放しません。 呼び出しでエラーが発生しない場合、呼び出し元プロバイダーまたはゲートウェイは [、MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって **STnefProblemArray** のメモリを解放する必要があります。 
  
## <a name="see-also"></a>関連項目



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[SPropTagArray](sproptagarray.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

