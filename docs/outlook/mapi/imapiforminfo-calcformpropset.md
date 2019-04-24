---
title: IMAPIFormInfoCalcFormPropSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcFormPropSet
api_type:
- COM
ms.assetid: cc3ffb8d-9cc4-47d3-9aa9-02c3a5b7775c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0b62c21348da71c1ee863f70d6e6a549a5d10003
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342127"
---
# <a name="imapiforminfocalcformpropset"></a>IMAPIFormInfo::CalcFormPropSet

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームが使用するプロパティの完全なセットへのポインターを返します。
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppFormPropArray
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 返される文字列は、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
 _ppformproparray_
  
> 読み上げ返された[smapiformproparray](smapiformproparray.md)の構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|mfcoutput .cpp  <br/> |出力 forminfo (_c)  <br/> |mfcmapi は、フォーム情報オブジェクトのデバッグ出力を作成するときに**imapiforminfo:: CalcFormPropSet**メソッドを使用します。  <br/> |
   
## <a name="see-also"></a>関連項目



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

