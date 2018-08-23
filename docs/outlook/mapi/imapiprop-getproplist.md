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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5417853dbb1fa87d2beead2f73ca57329e17b044
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571123"
---
# <a name="imapipropgetproplist"></a>IMAPIProp::GetPropList

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
すべてのプロパティのプロパティ タグを返します。 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]返されるプロパティは、タグ内の文字列の書式を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> 関数が返す文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
 _lppPropTagArray_
  
> [out]オブジェクトのプロパティのすべてのタグを含むプロパティ タグ配列へのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロパティ タグのすべてが正常に返されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。
    
## <a name="remarks"></a>注釈

**IMAPIProp::GetPropList**メソッドは、現在のオブジェクトによってサポートされている各プロパティのプロパティ タグを取得します。 オブジェクトは、任意のプロパティを現在サポートしていません、 **getproplist メソッド**は**あう**メンバーが 0 に設定するプロパティ タグ配列を返します。 
  
**Getproplist メソッド**から返されるプロパティのスコープは、プロバイダーによって異なります。 一部のサービス プロバイダーは、呼び出し元がアクセス権を持たないこれらのプロパティを除外します。 すべてのプロバイダーでは、 **PT_OBJECT**の種類のプロパティが返されます。
  
オブジェクトが Unicode をサポートしていない場合、 **getproplist メソッド**は、オブジェクトに対して定義されている文字列のプロパティがない場合でも、MAPI_E_BAD_CHARWIDTH を返します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

リモート トランスポート プロバイダーは、ここで指定どおり正確に**getproplist メソッド**を実装します。 特別な懸念事項はありません。 実装では、同じように[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドでサポートされているプロパティの一覧を返しますは、もちろん。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_LppPropTagArray_で指定されたプロパティ タグ配列を解放する[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI は、 **GetProps**に渡すプロパティの一覧を取得するのに**IMAPIProp::GetPropList**メソッドを使用します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

