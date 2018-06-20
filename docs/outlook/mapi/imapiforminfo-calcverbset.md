---
title: IMAPIFormInfoCalcVerbSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcVerbSet
api_type:
- COM
ms.assetid: 0170dc9d-dc72-48e2-a522-374f199b18ea
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 362afb1efeddeae72cc19256c377cb2c0f7ecba0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800540"
---
# <a name="imapiforminfocalcverbset"></a>IMAPIFormInfo::CalcVerbSet

  
  
**適用されます**: Outlook 
  
フォームを使用する動詞の完全なセットへのポインターを返します。
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]返される文字列の種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> 関数が返す文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
 _ppMAPIVerbArray_
  
> [out]フォームの動詞が含まれている返された[SMAPIVerbArray](smapiverbarray.md)構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。
    
## <a name="remarks"></a>備考

クライアント アプリケーションは、フォームで使用されている動詞のセットへのポインターを取得する**IMAPIFormInfo::CalcVerbSet**メソッドを呼び出します。 _PpMAPIVerbArray_パラメーターに返される**SMAPIVerbArray**構造で、動詞がインデックス番号の順に返されます。**lVerb**メンバーでは、各動詞のインデックスが検索されます。 クライアント アプリケーションでは、動的にメニューを作成、非表示にするまたはボタンを表示すると、動詞の配列を使用できます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MFCOutput.cpp  <br/> |_OutputFormInfo  <br/> |MFCMAPI では、オブジェクトの情報をフォームのデバッグ出力の書き込み中に、 **IMAPIFormInfo::CalcVerbSet**メソッドを使用します。  <br/> |
   
## <a name="see-also"></a>関連項目



[SMAPIVerbArray](smapiverbarray.md)
  
[IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

