---
title: IAddrBookPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.PrepareRecips
api_type:
- COM
ms.assetid: d423f7b5-23b8-44dd-bca3-6590182dc42d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 461cd536641e338cd29c849bb8069d3ac34f1667
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613955"
---
# <a name="iaddrbookpreparerecips"></a>IAddrBook::PrepareRecips

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージング システムで後で使用する受信者リストを準備します。 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]エントリの開き方を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_CACHE_ONLY
  
> 名前解決を実行するには、オフライン アドレス帳のみを使用します。 たとえば、このフラグを使用すると、クライアント アプリケーションがキャッシュされた Exchange モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成せずにキャッシュからそのアドレス帳内のエントリにアクセスできます。 このフラグは、アドレス帳プロバイダー Exchangeサポートされます。
    
 _lpSPropTagArray_
  
> [in]更新が必要なプロパティを示すプロパティ タグの配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター。 _lpSPropTagArray パラメーター_ には NULL を指定できます。 
    
 _lpRecipList_
  
> [in]受信者の一覧 [を含む ADRLIST](adrlist.md) 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 受信者リストが正常に準備されました。
    
## <a name="remarks"></a>注釈

クライアントとサービス プロバイダーは **PrepareRecips メソッドを呼び** 出して、次の操作を実行します。 
  
- _lpRecipList_ パラメーター内のすべての受信者に、長期的なエントリ識別子が設定されている必要があります。 
    
- _lpRecipList_ パラメーターの各受信者に _、lpSPropTagArray_ パラメーターにリストされているプロパティが含み、これらのプロパティが受信者リストの最初に表示されます。 
    
MAPI は、各受信者の短期エントリ識別子を長期エントリ識別子に変換します。 必要に応じて、受信者の長期エントリ識別子が適切なアドレス帳プロバイダーから取得され、追加のプロパティが要求されます。
  
個々の受信者エントリでは、要求されたプロパティが最初に順序付けされ、その後にエントリに既に存在していたプロパティが続きます。 _lpSPropTagArray_ パラメーターで要求されたプロパティの 1 つ以上が適切なアドレス帳プロバイダーによって処理されない場合、プロパティの種類は PT_ERROR に設定されます。 プロパティの値は、プロパティを使用できないMAPI_E_NOT_FOUND特定の理由を示す別の値に設定されます。 _lpRecipList_ パラメーターに含まれる各 [SPropValue](spropvalue.md)構造体は [、MAPIAllocateBuffer](mapiallocatebuffer.md)関数と [MAPIAllocateMore](mapiallocatemore.md)関数を使用して個別に割り当て、個別に解放できる必要があります。 
  
プロパティの詳細についてはPT_ERRORプロパティの [種類を参照してください](property-types.md)。
  
## <a name="see-also"></a>関連項目



[ADRLIST](adrlist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[PidTagEntryId 標準プロパティ](pidtagentryid-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

