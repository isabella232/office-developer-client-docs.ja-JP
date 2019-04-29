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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: babff746af16d51ca154d049943f6be7e9fab589
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428782"
---
# <a name="imapiforminfocalcverbset"></a>IMAPIFormInfo::CalcVerbSet

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームが使用する動詞の完全なセットへのポインターを返します。
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 返される文字列は、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
 _ppMAPIVerbArray_
  
> 読み上げフォームの動詞を含む、返された[SMAPIVerbArray](smapiverbarray.md)構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。
    
## <a name="remarks"></a>注釈

クライアントアプリケーションは、 **imapiforminfo:: CalcVerbSet**メソッドを呼び出して、フォームで使用される動詞のセットへのポインターを取得します。 _ppMAPIVerbArray_パラメーターで返される**SMAPIVerbArray**構造体では、動詞がインデックス番号の順に返されます。各動詞のインデックスは、 **lverb**メンバにあります。 クライアントアプリケーションは、verb 配列を使用してメニューを動的に作成したり、ボタンを非表示または表示したりすることができます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|mfcoutput .cpp  <br/> |出力 forminfo (_c)  <br/> |mfcmapi は、フォーム情報オブジェクトのデバッグ出力を書き込むときに、 **imapiforminfo:: CalcVerbSet**メソッドを使用します。  <br/> |
   
## <a name="see-also"></a>関連項目



[SMAPIVerbArray](smapiverbarray.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

