---
title: PidTagProfileHomeServerFQDN 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: aef4a932da35f3c4955bc2f4b265b146775c6d87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341595"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a>PidTagProfileHomeServerFQDN 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイル構成の Kerberos 認証を有効にします。
  
****

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROFILE_HOME_SERVER_FQDN  <br/> |
|識別子:  <br/> |0x662A001F  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI プロファイルの構成  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティをユーザーのディレクトリ サーバーのドメイン名に設定すると、PR_PROFILE_AUTH_PACKAGE で **RPC_C_AUTHN_GSS_KERBEROS** を設定することにより、Microsoft Exchange Server 2007 以前のバージョンに対して Kerberos 認証を使用するように構成されているプロファイルに必要なドメイン コントローラー (DC) に直接接続できます。 
  
> [!NOTE]
> Microsoft Exchange Server 2010 および Exchange Server 2013 は、クライアント アクセス サーバーに対して行われたアドレス帳の呼び出しを、Exchange Server 2007 以前のバージョンで処理する方法とは異なる方法で処理します。 DSProxy プロセスは使用されなくなったので、Kerberos 認証が成功する可能性があります。 ただし、クライアントは DC と直接通信するのではなく、Exchange サーバーと通信します。これは望PR_PROFILE_HOME_SERVER_FQDNしません。  
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> コア メッセージ ストア オブジェクトに対して許容される操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

