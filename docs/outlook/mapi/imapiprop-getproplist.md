---
title: imapipropgetproplist
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetPropList
api_type:
- COM
ms.assetid: 0069c223-32bb-4286-b763-39fd45dc263b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f089fa2c608fb9fcb7deba2e061c5cf5886aa02f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414789"
---
# <a name="imapipropgetproplist"></a>IMAPIProp::GetPropList

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべてのプロパティのプロパティタグを返します。 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番返される property タグ内の文字列の形式を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 返される文字列は、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
 _lppPropTagArray_
  
> 読み上げすべてのオブジェクトのプロパティのタグを含む、プロパティタグ配列へのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> すべてのプロパティタグが正常に返されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。
    
## <a name="remarks"></a>注釈

**imapiprop:: getproplist**メソッドは、オブジェクトで現在サポートされている各プロパティの property タグを取得します。 オブジェクトが現在プロパティをサポートしていない場合、 **getproplist**は**cvalues**メンバーが0に設定されたプロパティタグ配列を返します。 
  
**getproplist**によって返されるプロパティの範囲は、プロバイダーによって異なります。 一部のサービスプロバイダーは、呼び出し元がアクセス権を持っていないプロパティを除外します。 すべてのプロバイダーは、 **PT_OBJECT**型のプロパティを返します。
  
オブジェクトが Unicode をサポートしていない場合、オブジェクトに対して定義されている文字列プロパティがない場合でも、 **getproplist**は MAPI_E_BAD_CHARWIDTH を返します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

リモートトランスポートプロバイダーは、ここで指定されたとおりに**getproplist**を実装します。 特別な問題はありません。 もちろん、実装では、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドでサポートされているのと同じプロパティのリストを返す必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、 _lppPropTagArray_によって示されるプロパティタグ配列を解放します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFunctions  <br/> |GetPropsNULL  <br/> |mfcmapi は、 **imapiprop:: getproplist**メソッドを使用して、 **GetProps**に渡すプロパティリストを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

