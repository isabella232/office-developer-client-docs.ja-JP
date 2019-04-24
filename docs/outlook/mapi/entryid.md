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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c77acb5226361ce31a7f6b1694de7fe23f8dd71b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315989"
---
# <a name="entryid"></a>ENTRYID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI オブジェクトのエントリ識別子を含みます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[cbnewentryid](cbnewentryid.md)、 [sizedentryid](sizedentryid.md) <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a>Members

 **abflags**
  
> オブジェクトを説明する情報を提供するフラグのビットマスク。 フラグの先頭バイトだけ ( **abflags [0]**) は、プロバイダーによって設定されます。他の3つは予約されています。 これらのフラグは、永続的なエントリ識別子に対して設定しないでください。これらは、短期的なエントリ識別子に対してのみ設定されます。 クライアントにとっては、この構造体は読み取り専用です。 次のフラグは、 **abflags [0]** で設定できます。
    
MAPI_NOTRECIP 
  
> このエントリ id は、メッセージの受信者として使用することはできません。
    
MAPI_NOTRESERVED 
  
> 他のユーザーは、エントリ識別子にアクセスできません。
    
MAPI_NOW 
  
> その他の場合は、エントリ識別子を使用することはできません。
    
MAPI_SHORTTERM 
  
> エントリ識別子は短い用語です。 このバイトの他のすべての値は、エントリ識別子の他の使用法が有効になっていない限り、設定する必要があります。
    
MAPI_THISSESSION 
  
> 他のセッションでは、エントリ識別子を使用できません。
    
 **l**
  
> サービスプロバイダーで使用されるバイナリデータの配列を示します。 クライアントアプリケーションは、この配列を使用できません。
    
## <a name="remarks"></a>解説

**ENTRYID**構造体は、オブジェクトに一意の識別子を作成するために、メッセージストアとアドレス帳プロバイダーによって使用されます。 エントリ識別子は、次の種類のオブジェクトを識別するために使用されます。 
  
- メッセージストア
    
- Folders
    
- メッセージ
    
- アドレス帳のコンテナー
    
- 配布リスト
    
- メッセージングユーザー
    
- 状態オブジェクト
    
- プロファイルセクション
    
各プロバイダーは、そのプロバイダーにとって意味のある**ENTRYID**構造の形式を使用します。 
  
1 つのオブジェクトは、2 つの異なるバイナリ値で表すことができるため、エントリ ID を直接比較することはできません。 2つのエントリ識別子が同じオブジェクトを表しているかどうかを判断するには、 [imapisession:: compareentryids](imapisession-compareentryids.md)メソッドを呼び出します。 
  
クライアントがオブジェクトの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出してそのエントリ識別子を取得すると、オブジェクトは、エントリ識別子の最も永続的な形式を返します。 クライアントは、 **abflags**メンバの最初のバイトにフラグが設定されていないことを確認することによって、エントリ識別子が長期間であることを確認できます。 
  
クライアントがテーブル内の列を使用してエントリ識別子にアクセスする場合、このエントリ識別子は長期間ではなく短期である可能性が高くなります。 短期的なエントリ識別子を使用すると、現在の MAPI セッションでのみ、対応するオブジェクトを開くことができます。 クライアントは、すべてのフラグが**abflags**メンバーの最初のバイトに設定されていることを確認することによって、エントリ識別子が短縮されていることを確認できます。 
  
一部のエントリ識別子は短期的ですが、長期間使用します。 このようなエントリ識別子には、 **abflags**メンバーの最初のバイトに1つ以上の適切なフラグが設定されています。 
  
**ENTRYID**構造体は、 [FLATENTRY](flatentry.md)構造体に似ています。 ただし、次のような違いがあります。 
  
- **ENTRYID**構造体には、エントリ識別子のサイズは格納されません。**FLATENTRY**構造体があります。 
    
- **ENTRYID**構造は、フラグデータとその他のエントリ識別子を個別に格納します。**FLATENTRY**構造体は、フラグデータをエントリ id の残りの部分と共に格納します。 
    
- **ENTRYID**構造体は、パラメーターとして[imapiprop](imapipropiunknown.md)インターフェイスのメソッドと、次の openentry **** メソッドに渡されます。 [IABLogon:: openentry](iablogon-openentry.md)、 [IAddrBook:: openentry](iaddrbook-openentry.md)、 [IMAPIContainer:: openentry](imapicontainer-openentry.md)、 [imapisession:: openentry](imapisession-openentry.md)、 [imapisession:: openentry](imapisupport-openentry.md)、 [IMsgStore:: openentry](imsgstore-openentry.md)、 [IMSLogon:: openentry](imslogon-openentry.md)
    
- **ENTRYID**構造体は、ディスクにエントリ識別子を格納するために使用されます。 **FLATENTRY**構造体は、エントリ id をファイルに格納したり、バイトのストリームに渡したりするために使用されます。 
    
クライアントは常に、自然に配置されたエントリ識別子を渡す必要があります。 プロバイダーは、任意に調整されたエントリ識別子を処理する必要がありますが、クライアントはこの動作を想定してはいけません。 適切なアライメントエントリ識別子をメソッドに渡さないと、RISC プロセッサでアライメントエラーが発生する可能性があります。 
  
自然なアラインメント要素 (通常は8バイト) は、CPU によってサポートされる最大のデータ型であり、通常はシステムメモリアロケーターによって使用される同じ配置要因です。 自然に配置されたメモリアドレスを使用すると、配置エラーが発生することなく、そのアドレスでサポートされているすべてのデータ型に CPU がアクセスできます。 RISC cpu の場合、サイズ n バイトのデータ型は通常、n バイトの倍数になるように調整する必要があります。アドレスは n の偶数倍になります。
  
詳細については、「[エントリ識別子](mapi-entry-identifiers.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目



[FLATENTRY](flatentry.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[PidTagRecordKey 標準プロパティ](pidtagrecordkey-canonical-property.md)


[MAPI の構造](mapi-structures.md)

