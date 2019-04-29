---
title: IAddrBookPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.PrepareRecips
api_type:
- COM
ms.assetid: d423f7b5-23b8-44dd-bca3-6590182dc42d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: db1c23f33e604d6aafdd8a046566c7390c281ad8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414278"
---
# <a name="iaddrbookpreparerecips"></a>IAddrBook::PrepareRecips

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージングシステムで後で使用するために、受信者リストを準備します。 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番エントリが開かれる方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_CACHE_ONLY
  
> 名前解決を実行するには、オフラインアドレス帳のみを使用します。 たとえば、このフラグを使用して、クライアントアプリケーションが exchange キャッシュモードでグローバルアドレス一覧 (GAL) を開き、クライアントとサーバーの間のトラフィックを作成せずに、キャッシュからそのアドレス帳のエントリにアクセスできるようにすることができます。 このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。
    
 _lpSPropTagArray_
  
> 順番更新が必要なプロパティがある場合に、そのプロパティを示すプロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 _lpSPropTagArray_パラメーターは NULL にすることができます。 
    
 _lpRecipList_
  
> 順番受信者のリストを含む[adrlist](adrlist.md)構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 受信者リストが正常に準備されました。
    
## <a name="remarks"></a>注釈

クライアントおよびサービスプロバイダーは、 **PrepareRecips**メソッドを呼び出して次の処理を行います。 
  
- _lpRecipList_パラメーターのすべての受信者が長期間のエントリ識別子を持っていることを確認します。 
    
- _lpRecipList_パラメーターの各受信者の_lpSPropTagArray_パラメーターにプロパティがリストされていること、およびこれらのプロパティが受信者リストの先頭に表示されることを確認します。 
    
MAPI は、各受信者の短い用語エントリ識別子を長期のエントリ識別子に変換します。 必要に応じて、受信者の長期入力識別子が適切なアドレス帳プロバイダーから取得され、追加のプロパティが要求されます。
  
個別の受信者エントリでは、要求されたプロパティが最初に並べ替えられ、その後にエントリに既に存在していたプロパティが続きます。 _lpSPropTagArray_パラメーターで要求されたプロパティの1つ以上が、適切なアドレス帳プロバイダーによって処理されない場合は、そのプロパティの種類は PT_ERROR に設定されます。 プロパティの値は、MAPI_E_NOT_FOUND に設定されるか、プロパティが使用できないより具体的な理由を示す別の値に設定されます。 _lpRecipList_パラメーターに含まれる各[spropvalue](spropvalue.md)構造体は、 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数と[MAPIAllocateMore](mapiallocatemore.md)関数を使用して個別に割り当てる必要があります。これにより、個別に解放することができます。 
  
PT_ERROR の詳細については、「[プロパティの種類](property-types.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[ADRLIST](adrlist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[PidTagEntryId 標準プロパティ](pidtagentryid-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

