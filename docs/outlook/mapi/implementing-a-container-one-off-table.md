---
title: コンテナーの1回限りのテーブルの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 72dc73b6ed8519be2d8010544fdd5dc5b7b0f759
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332887"
---
# <a name="implementing-a-container-one-off-table"></a>コンテナーの1回限りのテーブルの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンテナーの1つに属する1回限りのテーブルにアクセスするために、MAPI はコンテナーの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **IMAPITable**で**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティを開きます。インターフェイス. クライアントアプリケーションがコンテナーに受信者を追加しようとしているときに、コンテナーは、1回限りのテーブルを返すように求められます。 コンテナーで受信者が許可されている場合、プロバイダーは、独自のテーブル実装を返すか、または[imapisupport:: getoneofftable](imapisupport-getoneofftable.md)を呼び出して MAPI 実装を取得できます。 
  
コンテナーの1回限りのテーブル内の一連のテンプレートは、特定のコンテナーが保持できる受信者の種類を反映している必要があります。 通常、これには1つまたは2つのテンプレート (個々のメッセージングユーザーまたは配布リストを作成するためのテンプレート) が含まれます。 これらのテンプレートのエントリ識別子は、 **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) および**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) プロパティに格納されています。 ただし、コンテナーはこれらの種類のエントリに制限されることはありません。 他の種類の受信者またはディレクトリなどの受信者以外のエントリを保持できます。 
  

