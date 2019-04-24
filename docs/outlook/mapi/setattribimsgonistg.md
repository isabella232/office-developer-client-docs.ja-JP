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
ms.openlocfilehash: 852ce31ba5ab02ff8f05dee25c9b32acb73130ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337969"
---
# <a name="setattribimsgonistg"></a>SetAttribIMsgOnIStg

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[OpenIMsgOnIStg](openimsgonistg.md)関数によって指定された[IMessage](imessageimapiprop.md)オブジェクトのプロパティの属性を設定または変更します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとメッセージストアプロバイダー  <br/> |
   
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
  
> 順番プロパティ属性が設定されているオブジェクトへのポインター。 
    
 _lpproptags_
  
> 順番プロパティタグの配列が含まれている[SPropTagArray](sproptagarray.md)構造体へのポインター。プロパティの属性が設定されているプロパティを示します。 
    
 _lpPropAttrs_
  
> 順番設定するプロパティ属性を一覧表示する[sproな trarray](spropattrarray.md)構造体へのポインター。 
    
 _lpppropproblems 問題_
  
> 読み上げプロパティの問題のセットを含む、返された[sprop問題の配列](spropproblemarray.md)構造体へのポインター。 この構造体は、 **SetAttribIMsgOnIStg**が一部のプロパティを設定できた場合に発生する問題を特定します。ただし、すべてではありません。 _lpppropproblems_パラメーターに NULL へのポインターが渡された場合、一部のプロパティが設定されていない場合でも、プロパティ問題の配列は返されません。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは全体的に成功しましたが、1つ以上のプロパティがアクセスできず、PT_ERROR のプロパティの種類で返されました。
    
## <a name="remarks"></a>解説

property 属性は、プロパティオブジェクト (つまり、 [imapiprop: IUnknown](imapipropiunknown.md)インターフェイスを実装するオブジェクト) にのみアクセスできます。 ole 構造化ストレージオブジェクトで MAPI プロパティを使用できるようにするために、 [OpenIMsgOnIStg](openimsgonistg.md)は、ole **IStorage**オブジェクトの先頭に[IMessage: imapiprop](imessageimapiprop.md)オブジェクトをビルドします。 このようなオブジェクトのプロパティ属性は、 **SetAttribIMsgOnIStg**を使用して設定または変更したり、 [GetAttribIMsgOnIStg](getattribimsgonistg.md)で取得したりできます。 
  
 **メモ****GetAttribIMsgOnIStg**および**SetAttribIMsgOnIStg**は、すべての**IMessage**オブジェクトでは動作しません。 これらは、 **OpenIMsgOnIStg**によって返される**** **IMessage**オブジェクトに対してのみ有効です。 
  
_lpPropAttrs_パラメーターでは、属性の数と位置が、 _lpproptags_パラメーターで渡されるプロパティタグの数と位置に一致する必要があります。 
  
**SetAttribIMsgOnIStg**関数は、 **IMessage**スキーマで必要な場合にメッセージプロパティを読み取り専用にするために使用されます。 サンプルメッセージストアプロバイダーは、これを目的として使用します。 詳細については、「[メッセージ](mapi-messages.md)」を参照してください。 
  

