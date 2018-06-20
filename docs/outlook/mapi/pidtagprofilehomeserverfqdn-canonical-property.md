---
title: PidTagProfileHomeServerFQDN の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 398ff2fd4bab49c8279e198e3efa416c53abda7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803189"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a>PidTagProfileHomeServerFQDN の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
プロファイル構成の Kerberos 認証を有効にします。
  
****

|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_PROFILE_HOME_SERVER_FQDN  <br/> |
|識別子:  <br/> |0x662A001F  <br/> |
|データを入力します。  <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |MAPI プロファイルの構成  <br/> |
   
## <a name="remarks"></a>備考

により直接接続するドメイン コント ローラー (DC)、Microsoft Exchange Server 2007 に対して Kerberos 認証を使用するように構成されたプロファイルに必要なユーザーのディレクトリ サーバーのドメイン名にこのプロパティを設定し、以前のバージョンで**PR_PROFILE_AUTH_PACKAGE**で**RPC_C_AUTHN_GSS_KERBEROS**を設定します。
  
> [!NOTE]
> Microsoft Exchange Server 2010 と Exchange Server 2013 は、アドレス帳からの呼び出しをクライアント アクセス サーバーとは異なるで Exchange Server 2007 と以前のバージョンを処理する方法を処理します。 DSProxy プロセスは使用されませんので、Kerberos 認証が成功することがあります。 ただし、クライアントがあると通信できている Exchange サーバーの代わりに直接、DC では、適さない場合があります: 設定**PR_PROFILE_HOME_SERVER_FQDN**がこれを回避できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> コア メッセージのストア オブジェクトの許可された操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

