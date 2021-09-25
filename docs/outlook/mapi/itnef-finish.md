---
title: ITnefFinish
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITnef.Finish
api_type:
- COM
ms.assetid: 01a868f4-afda-43ba-bc17-c33ae56b7b7d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 67c8540cf6901e3e077fd8fd269d155043b3c1ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561349"
---
# <a name="itneffinish"></a>ITnef::Finish

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
キューに入れ、待機Transport-Neutralのすべてのカプセル化形式 (TNEF) 操作の処理を終了します。 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpKey_
  
> [out]添付ファイルの **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) キー プロパティへのポインター。 TNEF カプセル化オブジェクトは、このキーを使用して、メッセージ内の添付ファイルと添付ファイルの配置タグを一致します。 このキーは、添付ファイルごとに一意である必要があります。
    
 _lpProblem_
  
> [out]返される [STnefProblemArray 構造体へのポインターを指すポインター](stnefproblemarray.md) 。 **STnefProblemArray** 構造体は、適切にエンコードされていないプロパティがある場合は、どのプロパティを示します。 _lpProblem_ パラメーターに NULL が渡された場合、プロパティの問題の配列は返されません。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、予期される値または値を返しました。
    
## <a name="remarks"></a>注釈

トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイは **、ITnef::Finish** メソッドを呼び出して [、ITnef::AddProps](itnef-addprops.md) メソッドおよび [ITnef::SetProps](itnef-setprops.md) メソッドの呼び出しでエンコードが要求されたすべてのプロパティのエンコードを実行します。 TNEF オブジェクトが [OpenTnefStream](opentnefstream.md) 関数または [OpenTnefStreamEx](opentnefstreamex.md) 関数の TNEF_ENCODE フラグで開いた場合 **、Finish** メソッドは要求されたプロパティをそのオブジェクトに渡されたカプセル化ストリームにエンコードします。 TNEF オブジェクトを TNEF_DECODE フラグで開いた場合 **、Finish** メソッドは TNEF ストリームからプロパティをデコードし、所属するメッセージに書き戻します。 
  
Finish 呼 **び出** しの後、カプセル化ストリームへのポインターは TNEF データの末尾を指します。 プロバイダーまたはゲートウェイが Finish 呼び出し後に TNEF ストリーム データを使用する必要がある場合は、ストリーム ポインターを TNEF ストリーム データの先頭にリセットする必要があります。  
  
TNEF 実装は、終了プロセスを停止せずに TNEF ストリーム エンコードの問題を **報告** します。 _lpProblem_ パラメーターで返される [STnefProblemArray](stnefproblemarray.md)構造体は、処理できない TNEF 属性または MAPI プロパティを示します (指定されている場合)。 **STnefProblemArray** に含まれる **STnefProblem** 構造体の scode メンバーで返される値は、特定の問題を示します。  プロバイダーまたはゲートウェイは **、Finish** が問題レポートを返していないすべてのプロパティまたは属性が正常に処理されたという前提で作業できます。 
  
プロバイダーまたはゲートウェイが問題の配列で動作しない場合は  _、lpProblem で NULL を渡す可能性があります_。この場合、問題のある配列は返されません。 
  
_lpProblem_ で返される値は、呼び出しが無効な値を返すS_OK。 このS_OK返される場合、プロバイダーまたはゲートウェイは **、STnefProblemArray** 構造体で返される値を確認する必要があります。 呼び出しでエラーが発生した場合 **、STnefProblemArray** 構造体は入力されないので、呼び出し元プロバイダーまたはゲートウェイは構造体を使用または解放しません。 呼び出しでエラーが発生しない場合、呼び出し元プロバイダーまたはゲートウェイは [、MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって **STnefProblemArray** のメモリを解放する必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI は **、ITnef::Finish** メソッドを使用して、新しい TNEF ストリームの処理を終了します。  <br/> |
   
## <a name="see-also"></a>関連項目



[ITnef::AddProps](itnef-addprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagAttachNumber 標準プロパティ](pidtagattachnumber-canonical-property.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

