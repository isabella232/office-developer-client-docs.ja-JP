---
title: itneffinoff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.Finish
api_type:
- COM
ms.assetid: 01a868f4-afda-43ba-bc17-c33ae56b7b7d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5b76f9daec89e9229fc7f81e1332c3075c951067
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348588"
---
# <a name="itneffinish"></a>ITnef::Finish

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
キューに入って待機しているすべてのトランスポート中立カプセル化形式 (TNEF) 操作の処理を完了します。 
  
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
    
 _lpkey_
  
> 読み上げ添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) キープロパティへのポインター。 TNEF カプセル化オブジェクトは、このキーを使用して、添付ファイルをメッセージの添付ファイル配置タグに一致させます。 このキーは、各添付ファイルに対して一意である必要があります。
    
 _lpproblem_
  
> 読み上げ返された[STnefProblemArray](stnefproblemarray.md)構造体へのポインターへのポインター。 **STnefProblemArray**構造体は、どのプロパティが適切にエンコードされなかったかを示します。 _lpproblem_パラメーターで NULL が渡された場合、プロパティ問題の配列は返されません。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、予想される値または値が返されました。
    
## <a name="remarks"></a>解説

トランスポートプロバイダー、メッセージストアプロバイダー、ゲートウェイは、ITnef:: [addprops](itnef-addprops.md)メソッドと[ITnef:: setprops](itnef-setprops.md)メソッドの呼び出しでエンコードが要求されたすべてのプロパティのエンコードを実行するために、 **:: Finish**メソッドを呼び出します。 [OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の TNEF_ENCODE フラグを使用して TNEF オブジェクトが開かれた場合、 **Finish**メソッドは、要求されたプロパティをそのオブジェクトに渡されるカプセル化ストリームにエンコードします。 TNEF_DECODE フラグを使用して tnef オブジェクトを開いた場合、 **Finish**メソッドは tnef ストリームからプロパティをデコードし、それを所有するメッセージに書き込みます。 
  
**完了**呼び出しの後、カプセル化ストリームへのポインターは TNEF データの末尾を指します。 プロバイダーまたはゲートウェイが、**完了**呼び出しの後に tnef ストリームデータを使用する必要がある場合は、tnef ストリームデータの先頭にストリームポインターをリセットする必要があります。 
  
tnef 実装は、**終了**プロセスを停止することなく、tnef ストリームエンコードの問題を報告します。 _lpproblem_パラメーターで返される[STnefProblemArray](stnefproblemarray.md)構造は、どの TNEF 属性または MAPI プロパティ (存在する場合) を処理できなかったかを示します。 **STnefProblemArray**に含まれている**STnefProblem**構造体の**scode**メンバーで返される値は、特定の問題を示します。 プロバイダーまたはゲートウェイは、**完了**したすべてのプロパティまたは属性が問題レポートを正常に処理したことを前提として機能します。 
  
プロバイダーまたはゲートウェイが問題のあるアレイで動作しない場合は、 _lpproblem_で NULL を渡すことができます。この場合、問題の配列は返されません。 
  
_lpproblem_で返される値は、呼び出しが S_OK を返す場合にのみ有効です。 S_OK が返された場合、プロバイダーまたはゲートウェイは、 **STnefProblemArray**構造体で返される値をチェックする必要があります。 呼び出しでエラーが発生した場合、 **STnefProblemArray**構造体は入力されず、呼び出しプロバイダーまたはゲートウェイは構造を使用したり、解放したりすることはできません。 呼び出しでエラーが発生しない場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、呼び出しプロバイダーまたはゲートウェイが**STnefProblemArray**のメモリを解放する必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ファイル .cpp  <br/> |SaveToTNEF  <br/> |mfcmapi は、 **ITnef:: Finish**メソッドを使用して、新しい TNEF ストリームの処理を完了します。  <br/> |
   
## <a name="see-also"></a>関連項目



[ITnef::AddProps](itnef-addprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagAttachNumber 標準プロパティ](pidtagattachnumber-canonical-property.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

