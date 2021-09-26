---
title: IAddrBookResolveName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.ResolveName
api_type:
- COM
ms.assetid: a7823c16-efda-45c2-b931-3e1fbc823b0b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9b371214b9f782fcf0afab0943c4a0654a5716d8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610735"
---
# <a name="iaddrbookresolvename"></a>IAddrBook::ResolveName

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
名前解決を実行し、受信者リストの受信者にエントリ識別子を割り当てる。
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]ユーザーにあいまい性の解決を求めるダイアログ ボックスの親ウィンドウへのハンドルを指定すると表示されます。
    
 _ulFlags_
  
> [in]解決プロセスのさまざまな側面を制御するフラグのビットマスク。 次のフラグを設定できます。
    
AB_UNICODEUI
  
> _lpszNewEntryTitle が_ UNICODE 文字列を示します。 
    
MAPI_CACHE_ONLY
  
> 名前解決を実行するには、オフライン アドレス帳のみを使用します。 たとえば、このフラグを使用すると、クライアント アプリケーションがキャッシュされた Exchange モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成せずにキャッシュからそのアドレス帳のエントリにアクセスできます。 このフラグは、アドレス帳プロバイダー Exchangeサポートされます。
    
MAPI_DIALOG 
  
> ユーザーに追加の名前解決情報を求めるダイアログ ボックスを表示します。 このフラグが設定されていない場合、ダイアログ ボックスは表示されません。 
    
MAPI_UNICODE 
  
> アドレス一覧で返されるプロパティは、アドレス一覧ではなく、PT_UNICODE型PT_STRING8。 
    
 _lpszNewEntryTitle_
  
> [in]ユーザーに受信者の入力を求めるダイアログ ボックス内のコントロールのタイトルのテキストへのポインター。 タイトルは受信者の種類によって異なります。 _lpszNewEntryTitle パラメーター_ には NULL を指定できます。 
    
 _lpAdrList_
  
> [インアウト]解決する受信者名の一覧を含む [ADRLIST](adrlist.md) 構造体へのポインター。 この **ADRLIST 構造** は [、IAddrBook::Address メソッドによって作成](iaddrbook-address.md) できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 名前解決プロセスが成功しました。
    
MAPI_E_AMBIGUOUS_RECIP 
  
> _lpAdrList_ パラメーター内の少なくとも 1 つの受信者が、アドレス帳内の複数のエントリと一致しました。 通常、この値は、MAPI_DIALOGフラグが設定されている場合に返され、ダイアログ ボックスの表示は禁止されます。 
    
MAPI_E_NOT_FOUND 
  
> _lpAdrList_ パラメーター内の少なくとも 1 つの受信者を解決できません。 通常、この値は、MAPI_DIALOGフラグが設定されている場合に返され、ダイアログ ボックスの表示は禁止されます。 
    
## <a name="remarks"></a>注釈

クライアントとサービス プロバイダーは **ResolveName メソッドを呼び出** して、名前解決プロセスを開始します。 未解決のエントリは、まだエントリ識別子またはプロパティ [(PidTagEntryId)](pidtagentryid-canonical-property.md)プロパティ **PR_ENTRYIDエントリです**。
  
 **ResolveName** は  _、lpAdrList_ パラメーターで渡されたアドレス一覧内の未解決のエントリごとに、次のプロセスを実行します。 
  
1. 受信者のアドレスの種類が SMTP アドレス _(displayname_ @  _domain.top-level-domain)_ の形式に準拠している場合 **、ResolveName** は一時エントリ識別子を割り当てる。 
    
2. ResolveName は、PR_AB_SEARCH_PATH **(** [PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) プロパティ内の各コンテナーについて [、IABContainer::ResolveNames メソッドを呼び出](iabcontainer-resolvenames.md)します。 **ResolveNames は** 、未解決の各受信者の表示名を、そのエントリの 1 つに属する表示名と一致します。 
    
3. コンテナーが **ResolveNames** をサポートしていない **場合、ResolveName** は、プロパティ制限 ([PidTagAnr](pidtaganr-canonical-property.md)) PR_ANR を使用してコンテナーのコンテンツ **テーブル** を制限します。 この制限により、コンテナーは一致する受信者を検索する "最適な推測" タイプの検索を実行します。 すべてのコンテナーは、プロパティ **の制限** PR_ANR必要があります。 
    
4. コンテナーが複数の名前に一致する受信者を返す場合 **、ResolveName** は MAPI_DIALOG フラグが設定されている場合にダイアログ ボックスを表示し、ユーザーが正しい名前を選択できます。 
    
5. PR_AB_SEARCH_PATH プロパティ **内のすべてのコンテナーが** 呼び出され、一致が見つからない場合、受信者は未解決のままです。 
    
1 つ以上の受信者が未解決の場合 **、ResolveName** は新しい受信者MAPI_E_NOT_FOUND。 1 つ以上の受信者が、ダイアログ ボックスで解決できないあいまいな解決策を持っていた場合、または MAPI_DIALOG フラグが設定されていない場合 **、ResolveName** は MAPI_E_AMBIGUOUS_RECIP を返します。 一部の受信者があいまいで解決できない場合 **、ResolveName** はどちらのエラー値も返す可能性があります。 
  
名前を解決できない場合、クライアントは、特別な形式のアドレスとエントリ識別子を持つ 1 回のアドレスを作成できます。 1 回きりエントリ識別子の形式の詳細については [、「One-Off Entry IDENTIFIERs」を参照してください](one-off-entry-identifiers.md)。 1 回のアドレスの形式の詳細については [、「One-Off Addresses 」を参照してください](one-off-addresses.md)。
  
MAPI では **、ADRLIST** の Unicode 文字文字列と ResolveName への新しいエントリ タイトル パラメーター **がサポートされています**。このフラグを設定MAPI_UNICODE、次のプロパティは [ADRENTRY](adrentry.md) 構造体の型PT_UNICODE返されます。 
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
ただし **、PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) プロパティは、常に型として返PT_STRING8。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI は **ResolveName** メソッドを使用して、メッセージに追加する前に 1 回のアドレスを解決します。  <br/> |
|MAPIABFunctions.cpp  <br/> |AddRecipient  <br/> |MFCMAPI は **ResolveName メソッドを使用** して、表示名でアドレス帳エントリを検索します。  <br/> |
   
## <a name="see-also"></a>関連項目



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

