---
title: GetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: bb27b28a-b2bd-4d4a-b0bb-0692f3de8e16
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 16e85eabc067bd82f5fb89c917afaf2831c75673
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300470"
---
# <a name="getattribimsgonistg"></a>GetAttribIMsgOnIStg

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[OpenIMsgOnIStg](openimsgonistg.md)関数によって指定された[IMessage](imessageimapiprop.md)オブジェクトのプロパティの属性を取得します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとメッセージストアプロバイダー  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a>パラメーター

 _lpObject_
  
> 順番[OpenIMsgOnIStg](openimsgonistg.md)関数から取得した**IMessage**オブジェクトへのポインター。 
    
 _lpPropTagArray_
  
> 順番属性を取得するプロパティを示すプロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 
    
 _lppproことわざ trarray_
  
> 読み上げ取得したプロパティ属性を含む、返される[sproな trarray](spropattrarray.md)構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは全体的に成功しましたが、1つ以上のプロパティがアクセスできず、PT_ERROR のプロパティの種類で返されました。
    
## <a name="remarks"></a>解説

property 属性は、プロパティオブジェクト (つまり、 [imapiprop: IUnknown](imapipropiunknown.md)インターフェイスを実装するオブジェクト) にのみアクセスできます。 ole 構造化ストレージオブジェクトで MAPI プロパティを使用できるようにするために、 [OpenIMsgOnIStg](openimsgonistg.md)は、ole **IStorage**オブジェクトの先頭に[IMessage: imapiprop](imessageimapiprop.md)オブジェクトをビルドします。 このようなオブジェクトのプロパティ属性は、 [SetAttribIMsgOnIStg](setattribimsgonistg.md)を使用して設定または変更したり、 **GetAttribIMsgOnIStg**で取得したりできます。 
  
> [!NOTE]
> **GetAttribIMsgOnIStg**および**SetAttribIMsgOnIStg**は、すべての**IMessage**オブジェクトでは動作しません。 これらは、 **OpenIMsgOnIStg**によって返される**** **IMessage**オブジェクトに対してのみ有効です。 
  
_lpppro指定 trarray_パラメーターの属性の数と位置は、 _lpPropTagArray_パラメーターのプロパティタグの数と位置に対応しています。 
  

