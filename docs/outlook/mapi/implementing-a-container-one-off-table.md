---
title: コンテナー テーブルのOne-Offする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 62951a7c4330fb8e909e0b6b978c210a5f5c1938
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610497"
---
# <a name="implementing-a-container-one-off-table"></a>コンテナー テーブルのOne-Offする

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンテナーの 1 つに属する 1 回のテーブルにアクセスするには、MAPI はコンテナーの [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出して **、IMAPITable** インターフェイスを使用して **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティを開きます。 クライアント アプリケーションがコンテナーに受信者を追加しようとしている場合、コンテナーは 1 回きりテーブルを返す必要があります。 コンテナーで受信者が許可されている場合、プロバイダーは独自のテーブル実装を返すか [、IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) を呼び出して MAPI 実装を返します。 
  
コンテナーの一時テーブル内のテンプレートのセットは、特定のコンテナーが保持できる受信者の種類を反映する必要があります。 通常、これには 1 つまたは 2 つのテンプレート、個々のメッセージング ユーザーまたは配布リストを作成するためのテンプレートが含まれます。 これらのテンプレートのエントリ識別子は **、PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) および PR_DEF_CREATE_DL **(** [PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) プロパティに保持されます。 ただし、コンテナーは、これらの種類のエントリに限定されるわけではありません。 他の種類の受信者や、ディレクトリなどの受信者以外のエントリを保持できます。 
  

