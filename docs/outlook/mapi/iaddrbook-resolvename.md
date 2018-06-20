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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: aa72085c4e50fcef1f2d3da81e5409af3d55d89b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800376"
---
# <a name="iaddrbookresolvename"></a>IAddrBook::ResolveName

  
  
**適用されます**: Outlook 
  
宛先リスト内の受信者にエントリの識別子を割り当て、名前解決を実行します。
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in]、表示されるダイアログ ボックスの親ウィンドウへのハンドルのあいまいさを解決するのにはユーザーに確認する、指定した場合。
    
 _ulFlags_
  
> [in]解決プロセスのさまざまな側面を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
AB_UNICODEUI
  
> その_lpszNewEntryTitle_が UNICODE 文字列であることを示します。 
    
MAPI_CACHE_ONLY
  
> 名前解決を実行するのにには、オフライン アドレス帳のみを使用します。 たとえば、このフラグを使用すると、exchange キャッシュ モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスするのにクライアント アプリケーションを許可します。 このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。
    
MAPI_DIALOG 
  
> その他の名前解決情報をユーザーに確認するダイアログ ボックスが表示されます。 このフラグが設定されていない場合、ダイアログ ボックスは表示されません。 
    
MAPI_UNICODE 
  
> PT_STRING8 の代わりに PT_UNICODE の種類のアドレス] ボックスの一覧で返されるプロパティがあることを示します。 
    
 _lpszNewEntryTitle_
  
> [in]受信者を入力するように求めるダイアログ ボックスで、コントロールのタイトルのテキストへのポインター。 タイトルは、受信者の種類によって異なります。 _LpszNewEntryTitle_パラメーターは NULL にできます。 
    
 _lpAdrList_
  
> [out]解決するのには受信者の名前のリストを格納する[ADRLIST](adrlist.md)構造体へのポインター。 [IAddrBook::Address](iaddrbook-address.md)メソッドでは、この**ADRLIST**の構造体を作成できます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 名前解決の処理に成功しました。
    
これらが同じ 
  
> _LpAdrList_パラメーターで 1 つ以上の受信者には、アドレス帳に複数のエントリが一致します。 通常、MAPI_DIALOG フラグを設定すると、ダイアログ ボックスの表示を禁止する場合にこの値が返されます。 
    
MAPI_E_NOT_FOUND 
  
> _LpAdrList_パラメーターで 1 つ以上の受信者を解決できません。 通常、MAPI_DIALOG フラグを設定すると、ダイアログ ボックスの表示を禁止する場合にこの値が返されます。 
    
## <a name="remarks"></a>備考

クライアントとサービス ・ プロバイダーは、名前解決プロセスを開始する**ResolveName**メソッドを呼び出します。 未解決のエントリは、エントリがないまだエントリの識別子またはプロパティの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) です。
  
 **ResolveName**は、 _lpAdrList_パラメーターで渡されたアドレス一覧に未解決のエントリごとに次のプロセスを通過します。 
  
1. 受信者のアドレスの種類が SMTP アドレスの形式に準拠している場合 (_表示名_@ _domain.top ・ レベル ・ ドメイン_)、 **ResolveName**はそれに 1 回限りのエントリの識別子を割り当てます。 
    
2. **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) のプロパティ内の各コンテナーには、 **ResolveName**は、 [IABContainer::ResolveNames](iabcontainer-resolvenames.md)メソッドを呼び出します。 **ResolveNames**が表示名のエントリのいずれかに属しますが、未解決の各受信者の表示名を一致させようとするとします。 
    
3. コンテナーが**ResolveNames**をサポートしていない場合、 **ResolveName**は**PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティの制限を使用してコンテナーの内容のテーブルを制限します。 この制限には、「最適な推測」一致する受信者を検索する検索の種類を実行するコンテナーが発生します。 すべてのコンテナーには、 **PR_ANR**プロパティ制限をサポートする必要があります。 
    
4. コンテナーに複数の名前に一致する受信者が返されるとき**ResolveName**は、MAPI_DIALOG フラグが設定されて、ユーザーが正しい名前を選択できるようにする場合にダイアログ ボックスを表示します。 
    
5. すべての**PR_AB_SEARCH_PATH**プロパティのコンテナーが呼び出された場合は、一致するものが見つかりませんでした、受信者は未解決のままになります。 
    
1 つまたは複数の受信者が解決できない、 **ResolveName**は MAPI_E_NOT_FOUND を返します。 **ResolveName**は] ダイアログ ボックスでは、解決できませんでしたが、あいまいな解像度を 1 つまたは複数の宛先があった場合、MAPI_DIALOG フラグが設定されていないために、これらが同じを返します。 一部の受信者があいまいで、いくつかを解決することはできません、 **ResolveName**はいずれかのエラー値を返すことができます。 
  
名前を解決できない場合、クライアントは特別な形式のアドレスとエントリの識別子を持つ一時アドレスを作成できます。 一時エントリ id の形式の詳細については、 [1 回限りのエントリ Id](one-off-entry-identifiers.md)を参照してください。 一時アドレスの形式の詳細については、[一時アドレス](one-off-addresses.md)を参照してください。
  
MAPI の**ADRLIST**新しいエントリのタイトル**ResolveName**; 文字の Unicode 文字列をサポートしていますMAPI_UNICODE フラグを設定する場合は、 [ADRENTRY](adrentry.md)構造体の PT_UNICODE の種類として、次のプロパティが返されます。 
  
- **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME**([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
ただし、PT_STRING8 を型としては、 **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) のプロパティは常に返されます。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI では、メッセージに追加する前に 1 回限りのアドレスを解決するのには、 **ResolveName**メソッドを使用します。  <br/> |
|MAPIABFunctions.cpp  <br/> |AddRecipient  <br/> |MFCMAPI では、 **ResolveName**メソッドを使用して、表示名、アドレス帳エントリを検索します。  <br/> |
   
## <a name="see-also"></a>関連項目



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

