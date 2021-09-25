---
title: SetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: 683d0d00-1b93-445d-86ff-180a3e6d2323
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a6f7dd8c8e583841b6805a4dd0416703d79c087b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578656"
---
# <a name="setattribimsgonistg"></a>SetAttribIMsgOnIStg

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[OpenIMsgOnIStg](openimsgonistg.md)関数によって提供される[IMessage](imessageimapiprop.md)オブジェクトのプロパティの属性を設定または変更します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとメッセージ ストア プロバイダー  <br/> |
   
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
  
> [in]プロパティ属性が設定されているオブジェクトへのポインター。 
    
 _lpPropTags_
  
> [in]プロパティ属性が設定されているプロパティを示すプロパティ タグの配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター。 
    
 _lpPropAttrs_
  
> [in]設定する [プロパティ属性を示す SPropAttrArray](spropattrarray.md) 構造体へのポインター。 
    
 _lppPropProblems_
  
> [out]プロパティの問題のセットを含む、返される [SPropProblemArray](spropproblemarray.md) 構造体へのポインター。 この構造は **、SetAttribIMsgOnIStg** が一部のプロパティを設定できたが、すべてではない場合に発生する問題を識別します。 _lppPropProblems_ パラメーターに NULL へのポインターが渡された場合、一部のプロパティが設定されていない場合でも、プロパティの問題配列は返されません。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは全体的に成功しましたが、1 つ以上のプロパティにアクセスする必要が生じ、プロパティの種類が変更されたPT_ERROR。
    
## <a name="remarks"></a>注釈

プロパティ属性にアクセスできるのは、プロパティ オブジェクト、つまり [IMAPIProp : IUnknown](imapipropiunknown.md) インターフェイスを実装するオブジェクトのみです。 OLE 構造化ストレージ オブジェクトで MAPI プロパティを使用するために [、OpenIMsgOnIStg](openimsgonistg.md)は OLE **IStorage** オブジェクトの上に [IMessage : IMAPIProp](imessageimapiprop.md)オブジェクトを作成します。 このようなオブジェクトのプロパティ属性は **、SetAttribIMsgOnIStg** を使用して設定または変更し [、GetAttribIMsgOnIStg](getattribimsgonistg.md)を使用して取得できます。 
  
 **メモ****GetAttribIMsgOnIStg** および **SetAttribIMsgOnIStg** は、すべての **IMessage オブジェクトで動作しません**。 これらは **、OpenIMsgOnIStg** によって返される **IMessage**-on- **IStorage** オブジェクトでのみ有効です。 
  
_lpPropAttrs_ パラメーターでは、属性の数と位置が _lpPropTags_ パラメーターで渡されるプロパティ タグの数と位置と一致している必要があります。 
  
**SetAttribIMsgOnIStg** 関数は、IMessage スキーマで必要なときにメッセージ プロパティを読み取り **専用にするために使用** されます。 サンプル メッセージ ストア プロバイダーは、この目的のためにそれを使用します。 詳細については、「Messages」を [参照してください](mapi-messages.md)。 
  

