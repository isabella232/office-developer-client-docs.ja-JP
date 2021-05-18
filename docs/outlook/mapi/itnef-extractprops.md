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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5a01c65bbec061248537558257c66d1a90128b5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407502"
---
# <a name="itnefextractprops"></a>ITnef::ExtractProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
TNEF カプセル化からプロパティを抽出します。 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]プロパティのデコード方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
TNEF_PROP_EXCLUDE 
  
> lpPropList パラメーターで指定されていないすべての  _プロパティをデコード_ します。 
    
TNEF_PROP_INCLUDE 
  
> lpPropList で指定されたプロパティ  _をデコードします_。
    
 _lpPropList_
  
> [in]デコード操作に含めるプロパティまたはデコード操作から除外するプロパティの一覧へのポインター。
    
 _lpProblems_
  
> [out]返される [STnefProblemArray 構造体へのポインターを指すポインター](stnefproblemarray.md) 。 **STnefProblemArray** 構造体は、適切にエンコードされていないプロパティがある場合は、どのプロパティを示します。 _lpProblems_ パラメーターに NULL が渡された場合、プロパティの問題の配列は返されません。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、予期される値または値を返しました。
    
MAPI_E_CORRUPT_DATA 
  
> ストリームにデコードされるデータが破損しています。
    
## <a name="remarks"></a>注釈

トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイは **、ITnef::ExtractProps** メソッドを呼び出して [、OpenTnefStream](opentnefstream.md) 関数に渡されたメッセージまたは添付ファイルのカプセル化からプロパティを抽出 (つまり、デコード) します。 呼び出し元プロバイダーまたはゲートウェイは、デコードするプロパティの一覧を指定できます。 プロバイダーとゲートウェイは **ExtractProps** を使用して、添付ファイルの特別な処理に関する情報を提供することもできます。 
  
 **ExtractProps は****、OpenTnefStream** に渡された元のメッセージにデコードされたプロパティを設定します。 後続 **の ExtractProps 呼** び出しはメッセージに戻り、新しいプロパティの一覧を抽出します。 
  
[ITnef::AddProps](itnef-addprops.md)メソッドとは異なり **、ITnef::Finish** メソッドが呼び出されるまで要求されたアクションをキューに入れる場合 **、ExtractProps** メソッドは、呼び出された際にカプセル化されたプロパティを直ちにデコードします。 このため、カプセル化デコードのターゲット メッセージは比較的空である必要があります。 ターゲット メッセージ内の既存のプロパティは、カプセル化されたプロパティによって上書きされます。 
  
 **ExtractProps** は **、OpenTnefStream** または [OpenTnefStreamEx](opentnefstreamex.md) 関数の TNEF_DECODE フラグを使用して開くオブジェクトでのみサポートされます。 
  
TNEF 実装では **、ExtractProps** プロセスを停止せずに TNEF ストリーム エンコードの問題を報告します。 _lpProblems_ で返される [STnefProblemArray](stnefproblemarray.md)構造体は、処理できない TNEF 属性または MAPI プロパティを示します (指定されている場合)。 **STnefProblemArray** に含まれる **STnefProblem** 構造体の scode メンバーで返される値は、特定の問題を示します。  プロバイダーまたはゲートウェイは **、ExtractProps** が問題レポートを返していないすべてのプロパティまたは属性が正常に処理されたという前提で動作できます。 
  
> [!NOTE]
> MAPI カプセル化ブロック内のプロパティを処理できない場合、TNEF ストリームのデコード中にストリームが不当な状態になる場合は、カプセル化ブロックのデコードが停止され、問題が報告されます。 この種類の問題の問題配列には **、ulPropTag** メンバーの場合は 0L、ulAttribute メンバーの場合は 0L、scode メンバーには MAPI_E_UNABLE_TO_COMPLETE が `attMAPIProps` `attAttachment` **含** まれる。  ストリームのデコードは停止されません。MAPI カプセル化ブロックのデコードに注意してください。 ストリームのデコードは、次の属性ブロックで続行されます。 
  
プロバイダーまたはゲートウェイが問題の配列で動作しない場合は  _、lppProblems で NULL を渡す可能性があります_。この場合、問題のある配列は返されません。 
  
_lpProblems_ で返される値は、呼び出しが無効な値を返すS_OK。 このS_OK返される場合、プロバイダーまたはゲートウェイは **、STnefProblemArray** 構造体で返される値を確認する必要があります。 呼び出しでエラーが発生した場合 **、STnefProblemArray** 構造体は入力されないので、呼び出し元プロバイダーまたはゲートウェイは構造体を使用または解放しません。 呼び出しでエラーが発生しない場合、呼び出し元プロバイダーまたはゲートウェイは [、MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって **STnefProblemArray** 構造体のメモリを解放する必要があります。 
  
## <a name="see-also"></a>関連項目



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::Finish](itnef-finish.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

