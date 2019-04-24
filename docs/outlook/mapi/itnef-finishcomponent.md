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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278887"
---
# <a name="itneffinishcomponent"></a>ITnef::FinishComponent

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージから1つずつ、トランスポートに依存しないカプセル化形式 (TNEF) ストリームに個々のコンポーネントを処理します。
  
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
  
> 順番終了するコンポーネントを制御するフラグのビットマスク。 次のフラグのいずれかまたは両方を設定する必要があります。
    
TNEF_COMPONENT_ATTACHMENT 
  
> attachment オブジェクトの処理が完了します。_ulComponentID_パラメーターには、添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティが含まれています。 
    
TNEF_COMPONENT_MESSAGE 
  
> メッセージオブジェクトの処理が完了します。 
    
 _ulComponentID_
  
> [in] 0 は、メッセージの処理を示します。または、処理される添付ファイルの**PR_ATTACH_NUM**プロパティです。 TNEF_COMPONENT_MESSAGE フラグが_ulflags_パラメーターで設定されている場合、 _ulComponentID_は0である必要があります。 
    
 _lpcustomproplist_
  
> 順番_lpcustomprops_パラメーターに渡されたプロパティを識別するプロパティタグを含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 lpcustomproplist パラメーターの_lpcustomprops_および property タグの各プロパティ値には、1対1で対応__ する必要があります。 
    
 _lpcustomprops_
  
> 順番エンコードするプロパティのプロパティ値を含む[spropvalue](spropvalue.md)構造体へのポインター。 
    
 _lpproplist_
  
> 順番エンコードするプロパティのプロパティタグを含む**SPropTagArray**構造体へのポインター。 
    
 _lppproblems 問題_
  
> 読み上げ返された[STnefProblemArray](stnefproblemarray.md)構造体へのポインターへのポインター。 **STnefProblemArray**構造体は、どのプロパティが適切にエンコードされなかったかを示します。 _lppproblems_パラメーターで NULL が渡された場合、プロパティ問題の配列は返されません。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>解説

トランスポートプロバイダー、メッセージストアプロバイダー、ゲートウェイは、 **ITnef:: finish コンポーネント**メソッドを呼び出して、1つのコンポーネント (メッセージまたは添付ファイル) に対して TNEF 処理を実行します。これは、 _ulflags_パラメーターに設定されているフラグによって示されます。 
  
コンポーネント処理を有効にするために、呼び出しプロバイダーまたはゲートウェイは、オブジェクトを開いてエンコードを受け取る[OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の_ulflags_の TNEF_COMPONENT_ENCODING フラグを渡します。 
  
_lpcustomproplist_パラメーターと_lpcustomprops_パラメーターの値を渡すと、 [ITnef:: setprops](itnef-setprops.md)メソッドによって実行されたコンポーネントエンコードは同じになります。 _lpproplist_パラメーターで値を渡すと、 [ITnef:: addprops](itnef-addprops.md)メソッドによって実行されるコンポーネントエンコードは、 _ulflags_で TNEF_PROP_INCLUDE フラグが設定された状態で実行されます。 これらの値を渡すと、複数の呼び出しではなく、1回の呼び出しでエンコードを実行できます。
  
tnef 実装は、終了**コンポーネント**プロセスを停止することなく、tnef ストリームエンコードの問題を報告します。 _lppproblems_で返される**STnefProblemArray**構造は、どの TNEF 属性または MAPI プロパティ (存在する場合) を処理できなかったかを示します。 **STnefProblemArray**に含まれている**STnefProblem**構造体の**scode**メンバーで返される値は、特定の問題を示します。 プロバイダーまたはゲートウェイは、終了**コンポーネント**が問題レポートを返さないすべてのプロパティまたは属性が正常に処理されたことを前提として機能します。 
  
プロバイダーまたはゲートウェイが問題のある配列で機能しない場合は、 _lppproblems_で NULL を渡すことができます。この場合、問題の配列は返されません。
  
_lppproblems_で返される値は、呼び出しが S_OK を返す場合にのみ有効です。 S_OK が返された場合、プロバイダーまたはゲートウェイは、 [STnefProblemArray](stnefproblemarray.md)構造体で返される値をチェックする必要があります。 呼び出しでエラーが発生した場合、 **STnefProblemArray**構造体は入力されず、呼び出しプロバイダーまたはゲートウェイは構造を使用したり、解放したりすることはできません。 呼び出しでエラーが発生しない場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、呼び出しプロバイダーまたはゲートウェイが**STnefProblemArray**のメモリを解放する必要があります。 
  
## <a name="see-also"></a>関連項目



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[SPropTagArray](sproptagarray.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

