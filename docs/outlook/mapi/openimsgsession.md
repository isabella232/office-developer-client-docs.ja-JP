---
title: OpenIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.OpenIMsgSession
api_type:
- COM
ms.assetid: f75229e3-5f44-4298-8706-9eddf0ef124c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 814884510fd2d5b4515c0a213c7a4f763617013e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584013"
---
# <a name="openimsgsession"></a>OpenIMsgSession

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
作成し、その中に作成されたメッセージをグループ分けするメッセージ セッションを開きます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a>パラメーター

 _lpMalloc_
  
> [in]OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) インターフェイスを公開するメモリ アロケーター オブジェクトへのポインター。 MAPI は、OLE IStorage インターフェイスを操作するときにこの割り当 [て方法を使用する必要](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) があります。 
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B 
    
 _lppMsgSess_
  
> [out]返されるメッセージ セッション オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK
  
> セッションが開かされました。
    
MAPI_E_INVALID_PARAMETER
  
>  _lpMalloc_ または  _lppMsgSess は_ NULL です。 
    
MAPI_E_INVALID_FLAGS
  
> 無効なフラグが渡された。
    
MAPI_UNICODE
  
> この関数を呼び出す場合、クライアントまたはサービス プロバイダーは、Unicode .msg ファイルMAPI_UNICODEフラグを設定します。 結果の [Imessage ファイル](imessageimapiprop.md) は、そのSTORE_UNICODE_OKにPR_STORE_SUPPORT_MASK Unicode プロパティをサポートします。 
    
## <a name="remarks"></a>注釈

メッセージ セッションは、いくつかの関連する MAPI IMessage ( 基になる OLE **IStorage** オブジェクトの上に構築された [IMAPIProp](imessageimapiprop.md)オブジェクト) を処理するクライアント アプリケーションおよびサービス プロバイダーによって使用されます。 クライアントまたはプロバイダーは **、OpenIMsgSession** 関数と [CloseIMsgSession](closeimsgsession.md) 関数を使用して、メッセージ セッション内でこのようなメッセージの作成をラップします。 メッセージ セッションを開いた後、クライアントまたはプロバイダーは [OpenIMsgOnIStg](openimsgonistg.md) への呼び出しでポインターを渡して、新しい **IMessage**-on- **IStorage** オブジェクトを作成します。 
  
メッセージ セッションでは、メッセージのすべての添付ファイルと他のプロパティに加えて、セッション中に作成された **すべての IMessage**-on- **IStorage** オブジェクトが追跡されます。 クライアントまたはプロバイダーが **CloseIMsgSession** を呼び出す場合、これらのオブジェクトはすべて閉じます。 **CloseIMsgSession** を呼び出す方法は **、IMessage**-on- **IStorage オブジェクトを閉じる唯一の方法** です。 
  
 **OpenIMsgSession** は、OLE **IStorage** オブジェクトとして複数の関連メッセージを処理する機能を必要とするクライアントおよびプロバイダーによって使用されます。 一度に 1 つのメッセージのみを開く場合は、複数のメッセージを追跡する必要はありません。 **また、OpenIMsgSession** を使用してメッセージ セッションを作成する理由はありません。 
  
基になる OLE オブジェクトを扱うので、MAPI は OLE メモリ割り当てを使用する必要があります。 OLE 構造化ストレージ オブジェクトと OLE メモリ割り当ての詳細については [、「OLE とデータ転送」を参照してください](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)。 
  

