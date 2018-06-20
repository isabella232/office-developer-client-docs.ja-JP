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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fe3e098b2b70e77bd0c536002a4724810261bff3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19800405"
---
# <a name="iaddrbookpreparerecips"></a>IAddrBook::PrepareRecips

  
  
**適用されます**: Outlook 
  
メッセージング システムによって後で使用できる受信者のリストを準備します。 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]エントリを開く方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_CACHE_ONLY
  
> 名前解決を実行するのにには、オフライン アドレス帳のみを使用します。 たとえば、このフラグを使用すると、exchange キャッシュ モードでグローバル アドレス一覧 (GAL) を開くと、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスするのにクライアント アプリケーションを許可します。 このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。
    
 _lpSPropTagArray_
  
> [in]更新する必要が存在する場合、プロパティを示すプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 _LpSPropTagArray_パラメーターは NULL にできます。 
    
 _lpRecipList_
  
> [in]受信者のリストを格納する[ADRLIST](adrlist.md)構造体へのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 宛先リストの準備ができました。
    
## <a name="remarks"></a>備考

クライアントとサービス ・ プロバイダーは、以下を実行する**PrepareRecips**メソッドを呼び出します。 
  
- _LpRecipList_パラメーター内のすべての受信者は、長期的なエントリの識別子であることを確認します。 
    
- _LpRecipList_パラメーターでは、各受信者が、 _lpSPropTagArray_パラメーターに表示されるプロパティを持っていると、受信者の一覧の先頭にこれらのプロパティが表示されることを確認します。 
    
MAPI では、長期のエントリ id を各受信者の短期的なエントリの識別子に変換します。 必要に応じて、適切なアドレス帳プロバイダーから受信者の長期のエントリ id を取得して、追加プロパティが要求されました。
  
個々 の受信者エントリ、要求されたプロパティの順序は最初に、後に既にエントリが存在していたすべてのプロパティ。 _LpSPropTagArray_パラメーターで要求されたプロパティのいずれかが適切なアドレス帳プロバイダーによって処理されない場合、そのプロパティの型が PT_ERROR に設定されます。 プロパティ値は MAPI_E_NOT_FOUND または具体的な理由がなぜ [のプロパティは利用できませんが、別の値に設定されます。 _LpRecipList_パラメーターに含まれる個々 の[SPropValue](spropvalue.md)構造体を個別に解放するために[MAPIAllocateBuffer](mapiallocatebuffer.md)と[MAPIAllocateMore](mapiallocatemore.md)関数を使用して個別に割り当てる必要があります。 
  
PT_ERROR 詳細については、[プロパティの型](property-types.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[ADRLIST](adrlist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[PidTagEntryId の標準的なプロパティ](pidtagentryid-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)

