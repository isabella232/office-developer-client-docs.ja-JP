---
title: アドレス帳のオプションの設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0d93fde7d654f0ee56dcda9f2fb69ad622e476dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593621"
---
# <a name="setting-address-book-options"></a>アドレス帳のオプションの設定

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
アドレス帳を使用するためのオプションについて説明する 3 つのプロパティを設定することができます。
  
- **PR_AB_SEARCH_PATH**([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))
    
    [IAddrBook::ResolveName](iaddrbook-resolvename.md)で**PR_AB_SEARCH_PATH**プロパティを使用して、名前解決、およびそれらに関連する注文に使用するコンテナーを決定します。 **PR_AB_SEARCH_PATH**内の各コンテナーには、 **IAddrBook::ResolveName**は、その[IABContainer::ResolveNames](iabcontainer-resolvenames.md)メソッドを呼び出します。 **PR_AB_SEARCH_PATH**の最後にコンテナーの前に**PR_AB_SEARCH_PATH**の先頭にコンテナーが検索されます。 
    
    [SRowSet](srowset.md)構造体、テーブル内の行を表すために使用するのと同じ構造を使用して、 **PR_AB_SEARCH_PATH**での検索順序を指定します。 [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)メソッドを呼び出して、現在の検索パスを表示し、 [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)メソッドを呼び出すことによって変更できます。 
    
- **PR_AB_DEFAULT_DIR**([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))
    
    **PR_AB_DEFAULT_DIR**プロパティは、アドレス帳が表示されるときに最初に表示するアドレス帳コンテナーのエントリの識別子です。 ディレクトリの既定の設定は、 [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)メソッドを呼び出すことによって変更するまで有効です。 既定のディレクトリを表示するには、 [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)メソッドを呼び出すことです。 
    
- **PR_AB_DEFAULT_PAB**([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))
    
これら 3 つのプロパティは、標準の**IMAPIProp**メソッドを使用してそれらを使用することはできませんので特殊です。 代わりに、 **IAddrBook**メソッドを使用する必要があります。 これらのプロパティの [なし] を変更するには**IMAPIProp::SetProps**でため、変更を永続的に**IMAPIProp::SaveChanges**を呼び出す必要はありません。 **IAddrBook**の方法で行われた変更は直ちに有効にします。 
  
## <a name="see-also"></a>関連項目



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

