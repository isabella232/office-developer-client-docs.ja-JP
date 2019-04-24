---
title: PidTagProfileHomeServerFQDN 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: '最終更新日時: 2015 年 3 月 9 日'
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
|識別子:  <br/> |0x662a001f  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI プロファイルの構成  <br/> |
   
## <a name="remarks"></a>解説

このプロパティをユーザーのディレクトリサーバーのドメイン名に設定すると、ドメインコントローラー (DC) への直接接続が許可されます。これは、Microsoft Exchange server 2007 に対して Kerberos 認証を使用するように構成されているプロファイルに必要です。以前のバージョンでは、 **PR_PROFILE_AUTH_PACKAGE**で**RPC_C_AUTHN_GSS_KERBEROS**を設定します。
  
> [!NOTE]
> Microsoft exchange server 2010 および exchange server 2013 は、クライアントアクセスサーバーに対して行われたアドレス帳呼び出しを、exchange server 2007 および以前のバージョンで処理する方法とは異なる方法で処理します。 DSProxy プロセスは使用されなくなったため、Kerberos 認証が成功する可能性があります。 ただし、クライアントは依然として DC ではなく Exchange サーバーと通信していますが、これは望ましくない場合があります。 **PR_PROFILE_HOME_SERVER_FQDN**を設定すると、これを回避できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> コアメッセージストアオブジェクトに対する許容される操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

