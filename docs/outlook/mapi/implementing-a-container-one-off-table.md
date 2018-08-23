---
title: コンテナーの 1 回限りのテーブルの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d468943f84f1d23f1b4b84881e69cee0041a5bae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576597"
---
# <a name="implementing-a-container-one-off-table"></a>コンテナーの 1 回限りのテーブルの実装

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
コンテナーの 1 つに属している一時テーブルにアクセスするには、MAPI は**IMAPITable**と**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) のプロパティを開くには、コンテナーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。インタ フェースです。 コンテナーがクライアント アプリケーションでコンテナーに受信者を追加しようとするときに、一時テーブルを取得しようとしています。 コンテナーは、いずれかの受信者を許可している場合、プロバイダー独自のテーブルの実装を返すか、MAPI 実装を取得する[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)を呼び出します。 
  
コンテナーの一時テーブル内のテンプレートのセットは、特定のコンテナーが保持できる受信者の種類を反映します。 通常、1 つまたは 2 つのテンプレート、個々 のメッセージングのユーザーまたは配布リストを作成するためのテンプレートが含まれます。 **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) と**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) のプロパティ] では、これらのテンプレートのエントリ id が保持されます。 ただし、コンテナーでは、これらの種類のエントリに限定されるわけではありませんです。 受信者または受信者以外のエントリは、ディレクトリなどの他の種類が格納できます。 
  

