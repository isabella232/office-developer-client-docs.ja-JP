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
ms.openlocfilehash: 9e17e8ef7df33ffa248eec4195c00c77d0c49f94
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587769"
---
# <a name="getattribimsgonistg"></a>GetAttribIMsgOnIStg

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
[OpenIMsgOnIStg](openimsgonistg.md)関数によって提供された[IMessage](imessageimapiprop.md)オブジェクトのプロパティの属性を取得します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション、およびメッセージ ストア プロバイダー  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a>パラメーター

 _lpObject_
  
> [in][OpenIMsgOnIStg](openimsgonistg.md)関数から取得した**IMessage**オブジェクトへのポインター。 
    
 _lpPropTagArray_
  
> [in]取得する対象の属性は、プロパティを示すプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 
    
 _lppPropAttrArray_
  
> [out]取得したプロパティの属性を格納する返された[SPropAttrArray](spropattrarray.md)構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは完了しましたが、1 つまたは複数のプロパティにアクセスできませんでしたし、PT_ERROR のプロパティの種類と返されました。
    
## <a name="remarks"></a>注釈

プロパティの属性は、プロパティ オブジェクト、つまり、オブジェクトを実装することでのみアクセスできます、 [IMAPIProp: IUnknown](imapipropiunknown.md)インタ フェースです。 [OpenIMsgOnIStg](openimsgonistg.md)ビルドの MAPI プロパティを OLE 構造化ストレージ オブジェクトで使用できるようにするのには、 [IMessage: IMAPIProp](imessageimapiprop.md) OLE **IStorage**オブジェクト上にあるオブジェクトです。 このようなオブジェクトのプロパティの属性の設定または[SetAttribIMsgOnIStg](setattribimsgonistg.md)に変更し、 **GetAttribIMsgOnIStg**を取得します。 
  
> [!NOTE]
> **IMessage**オブジェクトのすべては、 **GetAttribIMsgOnIStg**と**SetAttribIMsgOnIStg**は動作しません。 -点灯 - **OpenIMsgOnIStg**によって返される**IStorage**オブジェクトは、 **IMessage**に対して有効であるだけです。 
  
数と、 _lppPropAttrArray_パラメーター内の属性の位置の数と、 _lpPropTagArray_パラメーター内のプロパティ タグの位置に対応します。 
  

