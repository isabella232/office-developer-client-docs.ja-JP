---
title: IMAPIPropGetPropList
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
  
すべてのプロパティのプロパティ タグを返します。 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]返されるプロパティ タグ内の文字列の形式を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 返される文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
 _lppPropTagArray_
  
> [out]オブジェクトのすべてのプロパティのタグを含むプロパティ タグ配列へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> すべてのプロパティ タグが正常に返されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。
    
## <a name="remarks"></a>注釈

**IMAPIProp::GetPropList** メソッドは、オブジェクトで現在サポートされている各プロパティのプロパティ タグを取得します。 オブジェクトが現在プロパティをサポートしていない場合 **、GetPropList** は **cValues** メンバーが 0 に設定されたプロパティ タグ配列を返します。 
  
**GetPropList** によって返されるプロパティの範囲は、プロバイダーによって異なります。 一部のサービス プロバイダーは、呼び出し元がアクセスできないプロパティを除外します。 すべてのプロバイダーは、PT_OBJECT 型 **のプロパティを返します**。
  
オブジェクトが Unicode をサポートしていない場合 **、GetPropList** は、オブジェクトにMAPI_E_BAD_CHARWIDTH文字列プロパティが定義されていない場合でも、この値を返します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

リモート トランスポート プロバイダーは、 **ここで指定したとおりに GetPropList** を実装します。 特別な懸念はありません。 もちろん、実装では [、IMAPIProp::GetProps](imapiprop-getprops.md) メソッドでサポートされているのと同じプロパティの一覧を返す必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

[MAPIFreeBuffer 関数を呼び出](mapifreebuffer.md)して _、lppPropTagArray_ が指すプロパティ タグ配列を解放します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI は **IMAPIProp::GetPropList** メソッドを使用して **、GetProps** に渡すプロパティ リストを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

