---
title: アドレス帳のオプションの設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f72c916e917543b11089f8f5ef1aa4b9552a1b6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417344"
---
# <a name="setting-address-book-options"></a>アドレス帳のオプションの設定

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳を使用するためのオプションを説明する 3 つのプロパティを設定できます。
  
- **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))
    
    PR_AB_SEARCH_PATH **プロパティ** は [、IAddrBook::ResolveName](iaddrbook-resolvename.md) を使用して、名前解決に関与するコンテナーと、それに関係する順序を決定します。 **IAddrBook::ResolveName** **は**、PR_AB_SEARCH_PATH内の各コンテナーについて [、IABContainer::ResolveNames メソッドを呼び出](iabcontainer-resolvenames.md)します。 コンテナーは、PR_AB_SEARCH_PATHの **末尾** にあるコンテナーの前に検索 **PR_AB_SEARCH_PATH。** 
    
    テーブル内 **の行PR_AB_SEARCH_PATH** 表すのと同じ構造である [SRowSet](srowset.md) 構造体を使用して、検索順序を指定します。 現在の検索パスを表示するには [、IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) メソッドを呼び出し [、IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) メソッドを呼び出して変更します。 
    
- **PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))
    
    PR_AB_DEFAULT_DIR **プロパティ** は、アドレス帳の表示時に最初に表示されるアドレス帳コンテナーのエントリ識別子です。 既定のディレクトリ設定は [、IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) メソッドを呼び出して変更するまで有効です。 既定のディレクトリを表示するには [、IAddrBook::GetDefaultDir メソッドを呼び出](iaddrbook-getdefaultdir.md) します。 
    
- **PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))
    
これらの 3 つのプロパティは、標準の **IMAPIProp** メソッドを使用して処理できないので特別です。 代わりに **、IAddrBook メソッドを使用する** 必要があります。 **IMAPIProp::SetProps** を使用してこれらのプロパティを変更することはできませんので、変更を永続的に行うために **IMAPIProp::SaveChanges** を呼び出す必要はありません。 **IAddrBook メソッドを使用して行われた** 変更は、直ちに有効になります。 
  
## <a name="see-also"></a>関連項目



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

