---
title: IABLogonPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.PrepareRecips
api_type:
- COM
ms.assetid: 3c1845ea-e291-4855-9afd-51d2c64d7e85
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 82a7ecc8fbad0baf67b49c80c5a62cb8df94dfd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800353"
---
# <a name="iablogonpreparerecips"></a>IABLogon::PrepareRecips

**適用対象**: Outlook 
  
メッセージング システムによって後で使用できる受信者のリストを準備します。
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>�p�����[�^�[

_ulFlags_
  
> [in]返される文字列内のテキストの種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
  - MAPI_CACHE_ONLY: は、名前解決を実行するのには、オフライン アドレス帳のみを使用します。 たとえば、このフラグを使用すると、exchange キャッシュ モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスするのにクライアント アプリケーションを許可します。 このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。
    
_lpPropTagArray_
  
> [in]更新を必要とするプロパティを指定するプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 _LpPropTagArray_パラメーターは NULL にできます。 
    
_lpRecipList_
  
> [in]受信者の一覧を保持する[ADRLIST](adrlist.md)構造体へのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 宛先リストの準備ができました。
    
MAPI_E_NOT_FOUND 
  
> _LpRecipList_パラメーター内の受信者のいずれかが存在しません。 
    
## <a name="return-value"></a>戻り値

クライアントでは、1 つまたは複数の受信者のプロパティのセットを再配置を変更または MAPI の[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)メソッドを呼び出します。 受信者は、送信メッセージの受信者の一覧の一部ではないです。 MAPI は、アドレス帳プロバイダーの**IABLogon::PrepareRecips**メソッドへの呼び出しを転送します。 
  
**IABLogon::PrepareRecips**は、4 つの主要なタスクを実行します。 
  
- アドレス] ボックスの一覧のすべての受信者が指す_lpRecipList_パラメーターで、長期のエントリ id があることを保証します。 
    
- すべての受信者に、 _lpPropTagArray_パラメーターで指定されたプロパティ値の配列で指定されたプロパティがあることを保証します。 
    
- 呼び出しの前に存在していた他のすべてのプロパティの前に、プロパティ値の配列からプロパティが表示されることを保証します。
    
- 確実に**ADRLIST**構造体の各宛て先用の[ADRENTRY](adrentry.md)の構造体のプロパティの順序は、プロパティ値の配列の場合と同じです。 
    
_LpRecipList_パラメーターに**ADRENTRY**構造体には、受信者ごとに 1 つの**ADRENTRY**構造体が含まれています。 **ADRENTRY**の各構造体には、受信者のプロパティを記述する[SPropValue](spropvalue.md)構造体の配列が含まれています。 **IABLogon::PrepareRecips**が返されると、受信者ごとに**SPropValue**構造体の配列には、受信者の他のプロパティの後に_lpPropTagArray_からのプロパティが含まれています。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**IABLogon::PrepareRecips**を実装するには、プロパティの値を取得する、短期的なエントリの識別子を長期的なエントリの識別子に変換するプロパティを特定の順序で配置する必要があります。 _LpPropTagArray_パラメーターで要求されたプロパティは、 _lpRecipList_パラメーターで、各受信者の**ADRENTRY**の構造体に関連付けられているプロパティ値の配列の先頭にする必要があります。 これらのプロパティの値が存在しない場合のエントリ id を使用して、関連付けられているメッセージのユーザーまたは配布リストを開くし、欠落しているプロパティ値を取得します。 
  
渡された_lpRecipList_とは別に個別に構造体を解放することができるように、各**SPropValue**構造体を割り当てます。 **SPropValue**構造体に追加の空き領域を割り当てる必要があります場合、たとえば、文字列のプロパティのデータを格納するのに関数を使用[MAPIAllocateBuffer](mapiallocatebuffer.md)全プロパティの値の配列に追加の領域を割り当てます。 [MAPIFreeBuffer](mapifreebuffer.md)関数を使用して、元のプロパティ値の配列を解放して、 [MAPIAllocateMore](mapiallocatemore.md)関数を使用して必要な追加のメモリを割り当てることです。 
  
**IABLogon::PrepareRecips**を実装するには、次の手順を使用します。
  
1. _LpPropTagArray_パラメーターのエントリを確認します。 プロパティの値の配列が空の場合は、実行する作業はありません。 成功値を返します。 
    
2. _LpRecipList_パラメーターでは、各受信者を処理します。 リスト内の受信者ごとに 1 つの**ADRENTRY**構造体のメンバーがあります。 次の種類の受信者を無視するには。 
    
   - エントリ id、 **ADRENTRY**の構造 (つまり、未解決の受信者) の**rgPropVals**のメンバーでない受信者を指定します。 
    
   - プロバイダーに属していないエントリの識別子を持つ受信者。 これらの受信者は、別のアドレス帳プロバイダーに渡されます。
    
3. 受信者を開き、受信者に対して既に設定されているプロパティを取得します。
    
4. **GetProps**から返されるプロパティの配列を_lpRecipList_で指定されたプロパティ値の配列をマージします。 プロパティの両方のアレイでは、同じプロパティが発生する場合は、 _lpRecipList_の値を使用します。
    
5. _LpRecipList_プロパティの値の配列がすべての必要なプロパティを保持するのに十分な大きさの場合は、結合配列を使用して置き換えるだけです。 _LpRecipList_プロパティの値の配列が十分な大きさでない場合は、新しく割り当てられた配列を使用して交換してください。 新しい配列価値がある更新されたそれぞれの**あう**メンバーのことを確認してあります。 
    
6. _LpPropTagArray_パラメーターのプロパティのいずれかを認識していない場合は、プロパティの型を設定 PT_ERROR と MAPI_E_NOT_FOUND をまたはよりは、別の値にプロパティの値を受信者の**ADRENTRY**の構造体にプロパティの使用不可時間の特定の理由です。 PT_ERROR 詳細については、[プロパティの型](property-types.md)を参照してください。
    
> [!NOTE]
> **IABLogon::PrepareRecips**に渡される**ADRLIST**構造体を割り当て直すことはありませんか、エントリの数を変更します。 
  
## <a name="see-also"></a>関連項目

- [ADRLIST](adrlist.md)
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [PidTagEntryId 標準プロパティ](pidtagentryid-canonical-property.md)
- [SPropValue](spropvalue.md)
- [IABLogon : IUnknown](iablogoniunknown.md)

