---
title: SetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: 683d0d00-1b93-445d-86ff-180a3e6d2323
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e8a0daa2afe2397f39b7f37a31ef718ba65a3350
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803890"
---
# <a name="setattribimsgonistg"></a>SetAttribIMsgOnIStg

  
  
**適用対象**: Outlook 
  
[OpenIMsgOnIStg](openimsgonistg.md)関数によって提供された[IMessage](imessageimapiprop.md)オブジェクトのプロパティの属性を変更または設定します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション、およびメッセージ ストア プロバイダー  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a>パラメーター

 _lpObject_
  
> [in]属性が設定されているプロパティのオブジェクトへのポインター。 
    
 _lpPropTags_
  
> [in]属性が設定されているプロパティのプロパティを示すプロパティ タグの配列を格納する[SPropTagArray](sproptagarray.md)構造体へのポインター。 
    
 _lpPropAttrs_
  
> [in]設定するプロパティの属性を一覧表示する[SPropAttrArray](spropattrarray.md)構造体へのポインター。 
    
 _lppPropProblems_
  
> [out]返された[SPropProblemArray](spropproblemarray.md)構造体のプロパティの問題のセットが含まれているへのポインター。 この構造体は、 **SetAttribIMsgOnIStg**は、すべてではなく、一部のプロパティを設定することをされている場合に発生する問題を識別します。 _LppPropProblems_パラメーターに null ポインターが渡されると場合、は、いくつかのプロパティが設定されていない場合でもにプロパティの問題の配列が返されません。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは完了しましたが、1 つまたは複数のプロパティにアクセスできませんでしたし、PT_ERROR のプロパティの種類と返されました。
    
## <a name="remarks"></a>注釈

プロパティの属性は、プロパティ オブジェクト、つまり、オブジェクトを実装することでのみアクセスできます、 [IMAPIProp: IUnknown](imapipropiunknown.md)インタ フェースです。 [OpenIMsgOnIStg](openimsgonistg.md)ビルドの MAPI プロパティを OLE 構造化ストレージ オブジェクトで使用できるようにするのには、 [IMessage: IMAPIProp](imessageimapiprop.md) OLE **IStorage**オブジェクト上にあるオブジェクトです。 このようなオブジェクトのプロパティの属性の設定または**SetAttribIMsgOnIStg**に変更し、 [GetAttribIMsgOnIStg](getattribimsgonistg.md)を取得します。 
  
 **メモ****IMessage**オブジェクトのすべては、 **GetAttribIMsgOnIStg**と**SetAttribIMsgOnIStg**は動作しません。 -点灯 - **OpenIMsgOnIStg**によって返される**IStorage**オブジェクトは、 **IMessage**に対して有効であるだけです。 
  
_LpPropAttrs_パラメーターに番号と、属性の位置は数と、 _lpPropTags_パラメーターで渡されたプロパティ タグの位置が可能でなければなりません。 
  
**SetAttribIMsgOnIStg**関数を使用して、メッセージのプロパティを**IMessage**スキーマで必要なときは読み取り専用です。 サンプル メッセージ ストア プロバイダーは、この目的で使用します。 詳細については、[メッセージ](mapi-messages.md)を参照してください。 
  

