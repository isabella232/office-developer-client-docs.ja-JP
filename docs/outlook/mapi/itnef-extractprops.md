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
  
TNEF のカプセル化からプロパティを抽出します。 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番プロパティのデコード方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
TNEF_PROP_EXCLUDE 
  
> _lpproplist_パラメーターで指定されていないすべてのプロパティをデコードします。 
    
TNEF_PROP_INCLUDE 
  
> _lpproplist_で指定されたすべてのプロパティをデコードします。
    
 _lpproplist_
  
> 順番デコード操作に含めるまたは除外するプロパティのリストへのポインター。
    
 _lpproblems 問題_
  
> 読み上げ返された[STnefProblemArray](stnefproblemarray.md)構造体へのポインターへのポインター。 **STnefProblemArray**構造体は、どのプロパティが適切にエンコードされなかったかを示します。 lpproblems パラメーターで NULL が__ 渡された場合、プロパティ問題の配列は返されません。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、予想される値または値が返されました。
    
MAPI_E_CORRUPT_DATA 
  
> ストリームにデコードされるデータが破損しています。
    
## <a name="remarks"></a>注釈

トランスポートプロバイダー、メッセージストアプロバイダー、ゲートウェイは、 **ITnef:: ExtractProps**メソッドを呼び出して、メッセージまたは[OpenTnefStream](opentnefstream.md)関数に渡された添付ファイルのカプセル化から、プロパティを抽出 (デコード) します。 呼び出し元プロバイダーまたはゲートウェイは、デコードするプロパティのリストを指定できます。 プロバイダーとゲートウェイでは、 **ExtractProps**を使用して、添付ファイルの特別な処理に関する情報を提供することもできます。 
  
 **ExtractProps**は、デコードされたプロパティを使用して、 **OpenTnefStream**に渡される元のメッセージを設定します。 後続の**ExtractProps**呼び出しは、メッセージに戻り、プロパティの新しいリストを抽出します。 
  
[ITnef:: addprops](itnef-addprops.md)メソッドとは異なり、 **ITnef::: Finish**メソッドが呼び出されるまで、要求されたアクションをキューに入れます。 **ExtractProps**メソッドは、カプセル化されたプロパティを呼び出した直後にデコードします。 そのため、カプセル化デコードのターゲットメッセージは、比較的空である必要があります。 ターゲットメッセージ内の既存のプロパティは、カプセル化されたプロパティによって上書きされます。 
  
 **ExtractProps**は、 **OpenTnefStream**または[OpenTnefStreamEx](opentnefstreamex.md)関数の TNEF_DECODE フラグを使用して開かれたオブジェクトに対してのみサポートされています。 
  
tnef 実装は、 **ExtractProps**プロセスを停止することなく、tnef ストリームエンコードの問題を報告します。 _lpproblems_で返される[STnefProblemArray](stnefproblemarray.md)構造は、どの TNEF 属性または MAPI プロパティ (もしあれば) を処理できなかったかを示します。 **STnefProblemArray**に含まれている**STnefProblem**構造体の**scode**メンバーで返される値は、特定の問題を示します。 プロバイダーまたはゲートウェイは、 **ExtractProps**が問題レポートを返さないすべてのプロパティまたは属性が正常に処理されたことを前提として機能します。 
  
> [!NOTE]
> MAPI カプセル化ブロックのプロパティを処理できず、TNEF ストリームのデコード中にストリームが信頼されていない場合、カプセル化ブロックのデコードが停止され、問題が報告されます。 この種の問題に対する問題の配列には、 **ulPropTag** `attMAPIProps` `attAttachment`メンバーの0L、 **ulattribute**メンバー、および**scode**メンバーの MAPI_E_UNABLE_TO_COMPLETE が含まれています。 なお、ストリームのデコードは停止されず、MAPI カプセル化ブロックのデコードだけになります。 ストリームのデコードは、次の属性ブロックで続行されます。 
  
プロバイダーまたはゲートウェイが問題のある配列で機能しない場合は、 _lppproblems_で NULL を渡すことができます。この場合、問題の配列は返されません。 
  
_lpproblems 問題_で返される値は、呼び出しが S_OK を返す場合にのみ有効です。 S_OK が返された場合、プロバイダーまたはゲートウェイは、 **STnefProblemArray**構造体で返される値をチェックする必要があります。 呼び出しでエラーが発生した場合、 **STnefProblemArray**構造体は入力されず、呼び出しプロバイダーまたはゲートウェイは構造を使用したり、解放したりすることはできません。 呼び出しでエラーが発生しない場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、 **STnefProblemArray**構造体のメモリを呼び出しプロバイダーまたはゲートウェイが解放する必要があります。 
  
## <a name="see-also"></a>関連項目



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::Finish](itnef-finish.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

