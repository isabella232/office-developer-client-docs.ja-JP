---
title: MAPI ユーティリティの初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d0507a26b9ae5ae018111e2771e3af8b25761786
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567672"
---
# <a name="initializing-the-mapi-utilities"></a>MAPI ユーティリティの初期化

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI を使用する必要があるの一部にすぎませんが、ユーティリティ、インターフェイス、および機能は、MAPI の MAPIUTIL で宣言されています。H ヘッダー ファイルに**IPropData**や**ITableData**など、初期化するために**生じます**を呼び出す必要はありません。 詳細についてを参照してください[IPropData: IMAPIProp](ipropdataimapiprop.md)、 [ITableData: IUnknown](itabledataiunknown.md)と[生じます](mapiinitialize.md)。 代わりに、 **ScInitMapiUtil**関数を呼び出します。 詳細については、 [ScInitMapiUtil](scinitmapiutil.md)を参照してください。 **ScInitMapiUtil**は、ユーティリティ関数、および MAPI のアロケーターを必要とすることを要求しないで、明示的にメソッドを使用するクライアント アプリケーションを有効にします。 
  
シャット ダウン時に、 **DeinitMapiUtil**ユーティリティに接続しているリソースを解放するための呼び出しを確認します。 **MAPIUninitialize**を呼び出さないようにします。 詳細については、 [DeinitMapiUtil](deinitmapiutil.md)と[MAPIUninitialize](mapiuninitialize.md)を参照してください。
  
**ITableData**インタ フェースが**生じます**ではなく、 **ScInitMapiUtil**を呼び出したクライアント テーブルの通知をサポートしないことに注意します。 
  

