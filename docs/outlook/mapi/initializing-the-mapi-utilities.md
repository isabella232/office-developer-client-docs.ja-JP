---
title: MAPI ユーティリティを初期化しています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8ee0504d4a8b9e2ce96e42a53b778d4e3f518fcc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801064"
---
# <a name="initializing-the-mapi-utilities"></a>MAPI ユーティリティを初期化しています。

  
  
**適用されます**: Outlook 
  
MAPI を使用する必要があるの一部にすぎませんが、ユーティリティ、インターフェイス、および機能は、MAPI の MAPIUTIL で宣言されています。H ヘッダー ファイルに**IPropData**や**ITableData**など、初期化するために**生じます**を呼び出す必要はありません。 詳細についてを参照してください[IPropData: IMAPIProp](ipropdataimapiprop.md)、 [ITableData: IUnknown](itabledataiunknown.md)と[生じます](mapiinitialize.md)。 代わりに、 **ScInitMapiUtil**関数を呼び出します。 詳細については、 [ScInitMapiUtil](scinitmapiutil.md)を参照してください。 **ScInitMapiUtil**は、ユーティリティ関数、および MAPI のアロケーターを必要とすることを要求しないで、明示的にメソッドを使用するクライアント アプリケーションを有効にします。 
  
シャット ダウン時に、 **DeinitMapiUtil**ユーティリティに接続しているリソースを解放するための呼び出しを確認します。 **MAPIUninitialize**を呼び出さないようにします。 詳細については、 [DeinitMapiUtil](deinitmapiutil.md)と[MAPIUninitialize](mapiuninitialize.md)を参照してください。
  
**ITableData**インタ フェースが**生じます**ではなく、 **ScInitMapiUtil**を呼び出したクライアント テーブルの通知をサポートしないことに注意します。 
  

