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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351409"
---
# <a name="setting-address-book-options"></a>アドレス帳のオプションの設定

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
次の3つのプロパティを設定して、アドレス帳を使用するためのオプションを記述できます。
  
- **PR_AB_SEARCH_PATH**([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))
    
    **PR_AB_SEARCH_PATH**プロパティは[IAddrBook:: ResolveName](iaddrbook-resolvename.md)によって使用され、名前の解決に関係するコンテナーと、それらが関与する必要のある順序を決定します。 **PR_AB_SEARCH_PATH**の各コンテナーで、 **IAddrBook:: ResolveName**は[IABContainer:: ResolveNames](iabcontainer-resolvenames.md)メソッドを呼び出します。 **PR_AB_SEARCH_PATH**の先頭にあるコンテナーは、 **PR_AB_SEARCH_PATH**の末尾にあるコンテナーの前に検索されます。 
    
    **PR_AB_SEARCH_PATH**の検索順序は、テーブル内の行を表すために使用されるものと同じ構造を使用して、 [srowset](srowset.md)構造を使用して指定されます。 現在の検索パスを表示するには、 [IAddrBook:: GetSearchPath](iaddrbook-getsearchpath.md)メソッドを呼び出し、 [IAddrBook:: SetSearchPath](iaddrbook-setsearchpath.md)メソッドを呼び出して変更します。 
    
- **PR_AB_DEFAULT_DIR**([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))
    
    **PR_AB_DEFAULT_DIR**プロパティは、アドレス帳が表示されるときに最初に表示されるアドレス帳コンテナーのエントリ識別子です。 既定のディレクトリ設定は、 [IAddrBook:: SetDefaultDir](iaddrbook-setdefaultdir.md)メソッドを呼び出して変更するまで有効です。 [IAddrBook:: GetDefaultDir](iaddrbook-getdefaultdir.md)メソッドを呼び出すことで、既定のディレクトリを表示できます。 
    
- **PR_AB_DEFAULT_PAB**([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))
    
これら3つのプロパティは、標準の**imapiprop**メソッドを使用して操作できないため、特別なものになります。 代わりに、 **IAddrBook**メソッドを使用する必要があります。 これらのプロパティは、 **imapiprop:: setprops**で変更できないため、変更を永続的にするために**imapiprop:: SaveChanges**を呼び出す必要はありません。 **IAddrBook**メソッドを使用して加えた変更は、直ちに有効になります。 
  
## <a name="see-also"></a>関連項目



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

