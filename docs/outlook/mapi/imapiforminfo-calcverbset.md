---
title: IMAPIFormInfoCalcVerbSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormInfo.CalcVerbSet
api_type:
- COM
ms.assetid: 0170dc9d-dc72-48e2-a522-374f199b18ea
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9c7ecf9ae44cb19c6040b713fe77cfb6cf44a066
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551290"
---
# <a name="imapiforminfocalcverbset"></a>IMAPIFormInfo::CalcVerbSet

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームで使用される動詞の完全なセットへのポインターを返します。
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 返される文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
 _ppMAPIVerbArray_
  
> [out]フォームの動詞を含む [、返される SMAPIVerbArray](smapiverbarray.md) 構造体へのポインターを指すポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。
    
## <a name="remarks"></a>注釈

クライアント アプリケーションは **IMAPIFormInfo::CalcVerbSet** メソッドを呼び出して、フォームで使用される一連の動詞へのポインターを取得します。 ppMAPIVerbArray パラメーターで返される _SMAPIVerbArray_ 構造体では、動詞はインデックス番号の順に返されます。 各動詞のインデックスは、**その lVerb メンバーに見** つかりました。 クライアント アプリケーションでは、動詞配列を使用してメニューを動的に作成したり、ボタンを非表示または表示したりできます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MFCOutput.cpp  <br/> |_OutputFormInfo  <br/> |MFCMAPI は、フォーム情報オブジェクトのデバッグ出力を書き込む間に **IMAPIFormInfo::CalcVerbSet** メソッドを使用します。  <br/> |
   
## <a name="see-also"></a>関連項目



[SMAPIVerbArray](smapiverbarray.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

