---
title: ITnefFinish
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
ms.openlocfilehash: aff805f7868ec0c2adc55ece94c45b76368ba6eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583765"
---
# <a name="itneffinish"></a>ITnef::Finish

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
完了するとキューに登録されたすべてのトランスポート ニュートラル カプセル化形式 (TNEF) 操作を処理し、待機しています。 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpKey_
  
> [out]添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) のキーのプロパティへのポインター。 TNEF カプセル化オブジェクトは、メッセージ内の添付ファイルの配置タグの添付ファイルに一致するようにこのキーを使用します。 このキーは、添付ファイルごとに一意である必要があります。
    
 _lpProblem_
  
> [out]返された[STnefProblemArray](stnefproblemarray.md)構造体へのポインターへのポインター。 **STnefProblemArray**構造体は、どのプロパティでは、存在する場合、されたエンコードされません正しくを示します。 _LpProblem_パラメーターに NULL を渡した場合、プロパティの問題の配列は返されません。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値または値が返されます。
    
## <a name="remarks"></a>注釈

プロバイダー、メッセージ ストア プロバイダーでは、どのエンコーディングのすべてのプロパティのエンコーディングを実行する**ITnef::Finish**メソッドは、 [ITnef::AddProps](itnef-addprops.md)メソッドと[ITnef::SetProps](itnef-setprops.md)メソッドの呼び出しで要求されたゲートウェイの呼び出しを転送します。 TNEF オブジェクトは、 [OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の TNEF_ENCODE フラグを使用して開かれた、**完了**メソッドは要求されたプロパティをそのオブジェクトに渡されるカプセル化のストリームにエンコードします。 TNEF_DECODE フラグを使用して、TNEF オブジェクトが開かれた場合、**終了**メソッドは TNEF ストリームからプロパティをデコードしに属しているメッセージに書き戻されます。 
  
**終了**の呼び出しの後は、カプセル化のストリームへのポインターは、TNEF データの末尾を指します。 プロバイダーまたはゲートウェイは、呼び出しの**完了**後は、TNEF ストリーム データを使用する必要があるは TNEF ストリーム データの先頭に、ストリームのポインターをリセットする必要があります。 
  
TNEF の実装では、**終了**処理を停止することがなく TNEF ストリームのエンコーディングの問題を報告します。 _LpProblem_パラメーターに返された[STnefProblemArray](stnefproblemarray.md)構造体は、どの TNEF 属性または MAPI プロパティでは、存在する場合、処理できませんでしたを示します。 **STnefProblemArray**に含まれている**STnefProblem**の構造体のいずれかの**scode**メンバーの戻り値は、特定の問題を示します。 プロバイダーまたはゲートウェイは、すべてのプロパティまたは属性の対象の**終了**を返さない問題レポートが正常に処理されたことを前提として処理できます。 
  
_LpProblem_; で NULL を渡すことができます問題の配列を持つプロバイダーまたはゲートウェイが機能しない場合この例では、問題の配列は返されません。 
  
_LpProblem_で返される値は、呼び出しが S_OK を返す場合にのみ有効です。 S_OK が返されると、プロバイダーまたはゲートウェイは**STnefProblemArray**構造体で返される値を確認する必要があります。 呼び出しでエラーが発生した場合**STnefProblemArray**構造体が記入されていませんし、プロバイダーまたはゲートウェイが呼び出し元する必要があります使用または構造体を解放します。 呼び出しでエラーが発生しなかった場合、呼び出し元のプロバイダーまたはゲートウェイ必要がありますメモリを解放**STnefProblemArray**の[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI では、 **ITnef::Finish**メソッドを使用して、新しい TNEF ストリームの処理を完了します。  <br/> |
   
## <a name="see-also"></a>関連項目



[ITnef::AddProps](itnef-addprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagAttachNumber 標準プロパティ](pidtagattachnumber-canonical-property.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

