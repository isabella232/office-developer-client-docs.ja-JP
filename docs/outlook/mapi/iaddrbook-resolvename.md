---
title: IAddrBookResolveName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.ResolveName
api_type:
- COM
ms.assetid: a7823c16-efda-45c2-b931-3e1fbc823b0b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8a6a73153b857078cb37d94a634a6b0215a0a8c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287008"
---
# <a name="iaddrbookresolvename"></a>IAddrBook::ResolveName

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
名前解決を実行し、受信者リスト内の受信者にエントリ識別子を割り当てます。
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a>パラメーター

 _uluiparam_
  
> 順番ダイアログボックスの親ウィンドウへのハンドル。指定されている場合は、あいまいな解決をユーザーに求めるメッセージを表示します。
    
 _ulFlags_
  
> 順番解決プロセスのさまざまな側面を制御するフラグのビットマスク。 次のフラグを設定できます。
    
AB_UNICODEUI
  
> _lpsznewentrytitle_が UNICODE 文字列であることを示します。 
    
MAPI_CACHE_ONLY
  
> 名前解決を実行するには、オフラインアドレス帳のみを使用します。 たとえば、このフラグを使用して、クライアントアプリケーションが exchange キャッシュモードでグローバルアドレス一覧 (GAL) を開き、クライアントとサーバーの間のトラフィックを作成せずに、キャッシュからそのアドレス帳のエントリにアクセスできるようにすることができます。 このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。
    
MAPI_DIALOG 
  
> 追加の名前解決情報をユーザーに確認するダイアログボックスが表示されます。 このフラグが設定されていない場合は、ダイアログボックスは表示されません。 
    
MAPI_UNICODE 
  
> アドレス一覧で返されるプロパティが、PT_STRING8 ではなく PT_UNICODE 型であることを示します。 
    
 _lpsznewentrytitle_
  
> 順番ユーザーに受信者の入力を求めるダイアログボックス内のコントロールのタイトルを示すテキストへのポインター。 タイトルは、受信者の種類によって異なります。 _lpsznewentrytitle_パラメーターは NULL にすることができます。 
    
 _lpadrlist_
  
> [入力-出力]解決する受信者名のリストを含む[adrlist](adrlist.md)構造体へのポインター。 この**adrlist**構造は、 [IAddrBook:: Address](iaddrbook-address.md)メソッドによって作成できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 名前解決プロセスが正常に終了しました。
    
MAPI_E_AMBIGUOUS_RECIP 
  
> _lpadrlist_パラメーターの少なくとも1つの受信者が、アドレス帳の複数のエントリと一致しました。 通常、この値は、MAPI_DIALOG フラグが設定されているときに返され、ダイアログボックスの表示を禁止します。 
    
MAPI_E_NOT_FOUND 
  
> _lpadrlist_パラメーターの少なくとも1人の受信者を解決できません。 通常、この値は、MAPI_DIALOG フラグが設定されているときに返され、ダイアログボックスの表示を禁止します。 
    
## <a name="remarks"></a>解説

クライアントおよびサービスプロバイダーは、 **ResolveName**メソッドを呼び出して名前解決プロセスを開始します。 未解決のエントリとは、エントリ id または**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティをまだ持っていないエントリのことです。
  
 _lpadrlist_パラメーターに渡されたアドレス一覧の未解決の各エントリに対して、 **ResolveName**は次のプロセスを実行します。 
  
1. 受信者のアドレスの種類が SMTP アドレス ( _displayname_@ _ドメイン_) の形式に準拠している場合、 **ResolveName**は1回限りのエントリ識別子を割り当てます。 
    
2. **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) プロパティの各コンテナーに対して、 **ResolveName**は[IABContainer:: ResolveNames](iabcontainer-resolvenames.md)メソッドを呼び出します。 **ResolveNames**は、各受信者の表示名を、そのエントリのいずれかに属する表示名に一致させようとします。 
    
3. コンテナーが**ResolveNames**をサポートしていない場合、 **ResolveName**は、 **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティ制限を使用してコンテナーの contents テーブルを制限します。 この制限によって、コンテナーは一致する受信者を検索するために "最適な推測" の種類の検索を実行します。 すべてのコンテナーは、 **PR_ANR**プロパティ制限をサポートする必要があります。 
    
4. コンテナーが複数の名前に一致する受信者を返すと、MAPI_DIALOG フラグが設定されている場合、 **ResolveName**はダイアログボックスを表示し、ユーザーが正しい名前を選択できるようにします。 
    
5. **PR_AB_SEARCH_PATH**プロパティのすべてのコンテナーが呼び出され、一致が見つからない場合は、受信者は未解決のままになります。 
    
1つまたは複数の受信者が未解決の場合、 **ResolveName**は MAPI_E_NOT_FOUND を返します。 1つまたは複数の受信者があいまいな解決策をダイアログボックスで解決できない場合、または MAPI_DIALOG フラグが設定されていない場合、 **ResolveName**は MAPI_E_AMBIGUOUS_RECIP を返します。 一部の受信者があいまいで解決できない場合、 **ResolveName**はどちらかのエラー値を返すことができます。 
  
名前を解決できない場合、クライアントは、特別な形式のアドレスとエントリ識別子を持つ1回限りのアドレスを作成できます。 1回限りのエントリ識別子の形式の詳細については、「 [1 回限りのエントリ識別子](one-off-entry-identifiers.md)」を参照してください。 1回限りのアドレスの形式の詳細については、「[一時](one-off-addresses.md)アドレス」を参照してください。
  
MAPI では、 **adrlist**の Unicode 文字列と、 **ResolveName**への新しいエントリタイトルパラメーターがサポートされています。MAPI_UNICODE フラグを設定した場合、 [adrentry](adrentry.md)構造では、次のプロパティが PT_UNICODE 型として返されます。 
  
- **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME**([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
ただし、 **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) プロパティは常に PT_STRING8 型として返されます。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIABFunctions  <br/> |addoneoffaddress  <br/> |mfcmapi は、メッセージに追加する前に、 **ResolveName**メソッドを使用して、1回限りのアドレスを解決します。  <br/> |
|MAPIABFunctions  <br/> |AddRecipient  <br/> |mfcmapi は、 **ResolveName**メソッドを使用して、アドレス帳のエントリを表示名で検索します。  <br/> |
   
## <a name="see-also"></a>関連項目



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

