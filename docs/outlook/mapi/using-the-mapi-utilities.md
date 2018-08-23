---
title: MAPI ユーティリティの使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3f461d50e838aac0caee37d295ba8e86b9559bd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804207"
---
# <a name="using-the-mapi-utilities"></a>MAPI ユーティリティの使用

  
  
**適用対象**: Outlook 
  
MAPI ユーティリティでは、その他の機能をサポートするためにテーブルのデータとデータ オブジェクトのプロパティ、およびさまざまな機能の構成します。 これらのユーティリティを必要していないサービス ・ プロバイダーとの接続を確立するために MAPI サブシステムにログオンするクライアントのことができます。 API 関数[ScInitMapiUtil](scinitmapiutil.md)を呼び出す場合は、クライアントは、このカテゴリに適合して、初期化時に[生じます](mapiinitialize.md)関数ではなく。 
  
 **ScInitMapiUtil**は、MAPI のアロケーターを必要とするが、ことを要求しない、アロケーターに明示的に、ユーティリティ関数を使用するクライアントを有効にします。 シャット ダウンに時間がある場合は、 [MAPIUninitialize](mapiuninitialize.md)ではなく、リソースを解放するのには[DeinitMapiUtil](deinitmapiutil.md)を呼び出します。 **生じます**を呼び出すことはありませんクライアントは、 **MAPIUninitialize**を呼び出さないでください。
  
**生じます**ではなく、 **ScInitMapiUtil**を呼び出しています**IMAPITable**メソッドを使用せずに、 **ITableData**メソッドを使って、テーブルを使用するいるは、テーブルの通知は機能しないことに注意します。 通知は、MAPI ライブラリの使用を必要として[IMAPITable: IUnknown](imapitableiunknown.md)。
  

