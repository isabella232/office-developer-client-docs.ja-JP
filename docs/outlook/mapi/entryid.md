---
title: ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ENTRYID
api_type:
- COM
ms.assetid: 8ebb21ca-5ad1-4dcc-97b6-2390664b5d8d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c77acb5226361ce31a7f6b1694de7fe23f8dd71b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415272"
---
# <a name="entryid"></a>ENTRYID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI オブジェクトのエントリ識別子が含まれる。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CbNewENTRYID](cbnewentryid.md) [、SizedENTRYID](sizedentryid.md) <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a>Members

 **abFlags**
  
> オブジェクトを説明する情報を提供するフラグのビットマスク。 フラグの最初のバイト **abFlags[0]** だけがプロバイダーによって設定できます。他の 3 つは予約済みです。 これらのフラグは、永続的なエントリ識別子に対して設定する必要があります。これらは、短期エントリ識別子にのみ設定されます。 クライアントの場合、この構造は読み取り専用です。 **abFlags[0] では、次のフラグを設定できます**。
    
MAPI_NOTRECIP 
  
> エントリ識別子をメッセージの受信者として使用することはできません。
    
MAPI_NOTRESERVED 
  
> 他のユーザーは、エントリ識別子にアクセスできません。
    
MAPI_NOW 
  
> エントリ識別子は、他の時点では使用できません。
    
MAPI_SHORTTERM 
  
> エントリ識別子は短期的です。 エントリ識別子の他の使用が有効になっていない限り、このバイト内の他のすべての値を設定する必要があります。
    
MAPI_THISSESSION 
  
> エントリ識別子は、他のセッションでは使用できません。
    
 **ab**
  
> サービス プロバイダーによって使用されるバイナリ データの配列を示します。 クライアント アプリケーションでは、この配列を使用できません。
    
## <a name="remarks"></a>注釈

**ENTRYID 構造体は**、メッセージ ストアとアドレス帳プロバイダーがオブジェクトの一意の識別子を作成するために使用します。 エントリ識別子は、次の種類のオブジェクトを識別するために使用されます。 
  
- メッセージ ストア
    
- Folders
    
- メッセージ
    
- アドレス帳コンテナー
    
- 配布リスト
    
- メッセージング ユーザー
    
- 状態オブジェクト
    
- プロファイル セクション
    
各プロバイダーは、そのプロバイダーに合った **ENTRYID** 構造の形式を使用します。 
  
1 つのオブジェクトは、2 つの異なるバイナリ値で表すことができるため、エントリ ID を直接比較することはできません。 2 つのエントリ識別子が同じオブジェクトを表すかどうかを確認するには [、IMAPISession::CompareEntryIDs メソッドを呼び出](imapisession-compareentryids.md) します。 
  
クライアントがオブジェクトの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出してエントリ識別子を取得すると、オブジェクトはエントリ識別子の最も永続的な形式を返します。 クライアントは **、abFlags** メンバーの最初のバイトにどのフラグも設定されなかから、エントリ識別子が長期に設定されているのを確認できます。 
  
クライアントがテーブル内の列を通じてエントリ識別子にアクセスする場合、ほとんどの場合、このエントリ識別子は長期ではなく短期的です。 短期エントリ識別子を使用すると、現在の MAPI セッションでのみ対応するオブジェクトを開くことができます。 クライアントは **、abFlags** メンバーの最初のバイトにすべてのフラグが設定されているのを確認することで、エントリ識別子が短期的な状態を確認できます。 
  
一部のエントリ識別子は短期的ですが、長期的な使用があります。 このようなエントリ識別子には **、abFlags** メンバーの最初のバイトに 1 つ以上の適切なフラグが設定されます。 
  
**ENTRYID 構造体は** [FLATENTRY 構造に似](flatentry.md)ている。 ただし、いくつかの違いがあります。 
  
- **ENTRYID 構造体** は、エントリ識別子のサイズを格納しない。**FLATENTRY 構造体** は、次の動作を行います。 
    
- **ENTRYID 構造体は**、フラグ データとエントリ識別子の残りの部分を個別に格納します。**FLATENTRY 構造体は**、残りのエントリ識別子を持つフラグ データを格納します。 
    
- **ENTRYID** 構造体は [、IMAPIProp](imapipropiunknown.md)インターフェイスのメソッドおよび次の OpenEntry メソッドにパラメーターとして渡されます [。IABLogon::OpenEntry](iablogon-openentry.md)、 [IAddrBook::OpenEntry](iaddrbook-openentry.md)、 [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  、 [IMAPISession::OpenEntry](imapisession-openentry.md)、 [IMAPISupport::OpenEntry](imapisupport-openentry.md)、 [IMsgStore::OpenEntry](imsgstore-openentry.md)、 [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- ENTRYID **構造体は** 、エントリ識別子をディスクに格納するために使用されます。 **FLATENTRY 構造体は**、エントリ識別子をファイルに格納したり、バイト ストリームで渡したりするために使用されます。 
    
クライアントは、常に自然に配置されたエントリ識別子を渡す必要があります。 プロバイダーは任意に配置されたエントリ識別子を処理する必要があります。ただし、クライアントは、この動作を期待しない必要があります。 位置合わせされたエントリ識別子をメソッドに渡さない場合、RISC プロセッサで配置エラーが発生する可能性があります。 
  
自然な配置係数 (通常は 8 バイト) は、CPU でサポートされる最大のデータ型であり、通常はシステム メモリ アロケーターで使用されるのと同じ配置係数です。 自然に配置されたメモリ アドレスを使用すると、CPU は、そのアドレスでサポートしている任意のデータ型に、配置エラーを生成せずにアクセスできます。 RISC CPU の場合、サイズ N バイトのデータ型は通常、N バイトの倍数で配置され、アドレスは N の倍数である必要があります。
  
詳細については、「Entry [IDENTIFIERs」を参照してください](mapi-entry-identifiers.md)。 
  
## <a name="see-also"></a>関連項目



[FLATENTRY](flatentry.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[PidTagRecordKey 標準プロパティ](pidtagrecordkey-canonical-property.md)


[MAPI の構造](mapi-structures.md)

