---
title: エントリ ID
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1b55703c9ad12e3645e6e9cb3dcfcbdf21b90d25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800008"
---
# <a name="entryid"></a>エントリ ID

  
  
**適用されます**: Outlook 
  
MAPI オブジェクトのエントリ id が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CbNewENTRYID](cbnewentryid.md)、 [SizedENTRYID](sizedentryid.md) <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a>メンバー

 **abFlags**
  
> オブジェクトを説明する情報を提供するためのフラグのビットマスクです。 フラグ、 **abFlags [0]** の最初のバイトのみが、プロバイダーによって設定することが他の 3 つが予約されています。 永続的なエントリの識別子は、これらのフラグを設定しないでください。短期的なエントリの識別子にのみ設定されます。 クライアントにこの構造体は、読み取り専用です。 **AbFlags [0]** では、次のフラグを設定できます。
    
MAPI_NOTRECIP 
  
> エントリの識別子は、メッセージの受信者として使用できません。
    
MAPI_NOTRESERVED 
  
> 他のユーザーは、エントリの識別子にアクセスできません。
    
MAPI_NOW 
  
> それ以外の場合は、エントリの識別子を使用できません。
    
MAPI_SHORTTERM 
  
> エントリの識別子は、短期的です。 エントリの識別子の他の使用が有効でない場合、このバイトで他のすべての値を設定しなければなりません。
    
MAPI_THISSESSION 
  
> エントリの識別子は、他のセッションでは使用できません。
    
 **ab**
  
> サービス プロバイダーによって使用されるバイナリ データの配列を示します。 クライアント アプリケーションは、この配列を使用できません。
    
## <a name="remarks"></a>備考

**エントリ ID**の構造を使用してメッセージを格納し、アドレス帳プロバイダーは、オブジェクトの一意の識別子を作成します。 次の種類のオブジェクトを識別するエントリの識別子が使用されます。 
  
- メッセージ ・ ストア
    
- フォルダー
    
- メッセージ
    
- アドレス帳コンテナー
    
- 配布リスト
    
- ユーザーのメッセージング
    
- ステータス オブジェクト
    
- プロファイル セクション
    
各プロバイダーでは、そのプロバイダーに適した**エントリ ID**の構造体の形式を使用します。 
  
1 つのオブジェクトは、2 つの異なるバイナリ値で表すことができるため、エントリ ID を直接比較することはできません。 2 つのエントリ id が同じオブジェクトを表しているかどうかを確認するのには、 [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md)メソッドを呼び出します。 
  
クライアントは、そのエントリの識別子を取得するオブジェクトの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出す、ときにオブジェクトのエントリ id の最も永続的な形式を返します。 エントリ識別子は、 **abFlags**メンバーの最初のバイトに設定されているフラグのいずれかを確認することで長期的なクライアントを確認できます。 
  
クライアントには、このエントリの識別子は、長期的なのではなく短期的な多くの場合、テーブル内の列をエントリ id がアクセスするとします。 現在の MAPI セッションでのみ、対応するオブジェクトを開くには、短期的なエントリの識別子を使用できます。 クライアントは、エントリ識別子は、 **abFlags**メンバーの最初のバイトに設定されているすべてのフラグを確認することで短期的なことを確認できます。 
  
いくつかのエントリ id は短期的なが、長期的に使用されています。 このようなエントリ id は、 **abFlags**メンバーの最初のバイトに設定する適切なフラグの 1 つ以上があります。 
  
**エントリ ID**の構造体には、 [FLATENTRY](flatentry.md)構造体に似ています。 ただし、これにはいくつか相違点があります。 
  
- **エントリ ID**の構造体は、エントリ識別子のサイズを格納しません。**FLATENTRY**構造体は次のとおり行われます。 
    
- フラグ データおよびエントリの識別子の残りの部分に個別に格納**エントリ ID**の構造体**FLATENTRY**構造体は、フラグとデータ エントリの識別子の残りの部分を格納します。 
    
- [IMAPIProp](imapipropiunknown.md)インターフェイスのメソッドに、次の**OpenEntry**メソッドを**エントリ ID**の構造体がパラメーターとして渡された: [IABLogon::OpenEntry](iablogon-openentry.md)、[アドレス帳コンテナー](iaddrbook-openentry.md)、 [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)、 [IMAPISession::OpenEntry](imapisession-openentry.md)、 [IMAPISupport::OpenEntry](imapisupport-openentry.md)、 [IMsgStore::OpenEntry](imsgstore-openentry.md)、 [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- **エントリ ID**の構造体を使用すると、ディスク上のエントリ id を格納します。 エントリ識別子をファイルに格納するバイトのストリームに渡すことは、 **FLATENTRY**構造体が使用されます。 
    
クライアントは、必然的に配置されたエントリの識別子で常に渡す必要があります。 プロバイダーでは、任意に配置されたエントリの識別子を処理する必要がありますがクライアントにはこの現象は限りません。 適切なアライメントされたエントリの識別子をメソッドに渡すと可能性が整列エラー RISC プロセッサにします。 
  
自然な配置、8 バイト、通常は、CPU でサポートされる最大のデータ型と通常のシステム メモリ アロケーターによって使用される同じ配置係数。 自然にアラインメントされたメモリ アドレスでは、整列エラーを生成することがなくそのアドレスをサポートしている任意のデータ型にアクセスするために CPU を使用できます。 RISC cpu、サイズ N バイトのデータ型する必要があります通常に配置する、N バイトの倍数 N. の偶数の倍数の中のアドレスを持つ
  
詳細については、[エントリの識別子](mapi-entry-identifiers.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[FLATENTRY](flatentry.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[PidTagRecordKey の標準的なプロパティ](pidtagrecordkey-canonical-property.md)


[MAPI の構造](mapi-structures.md)

