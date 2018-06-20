---
title: サービス プロバイダーを開始します。
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 99f47ee4fe990b0e77fcf868977b72d83bfdbac7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804005"
---
# <a name="starting-a-service-provider"></a>サービス プロバイダーを開始します。

 
  
**適用されます**: Outlook 
  
ある時点で、クライアントで MAPI セッションを開始した後、サービス ・ プロバイダーが開始されます。 トランスポート プロバイダーは、クライアントがそのサービスの要求を行うときに開始されます。 アドレス帳、メッセージ ストア プロバイダーは、クライアントのログオン処理中に開始されます。
  
クライアントは、各プロファイルおよび特定のメッセージ ストア プロバイダーをロードするのには[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)に含まれているアドレス帳プロバイダーをロードする[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)を呼び出します。 メッセージ サービスの一部であるアドレス帳プロバイダーは、サービスの他のプロバイダーのいずれかの前に開始されます。 
  
MAPI は、次の手順でアクティブなプロファイルの各サービス プロバイダーを起動します。
  
- プロファイルにその DLL の名前を検索しています。 Mapisvc.inf の構成ファイルのプロファイルに表示されるように、プロバイダー DLL の名前を登録する必要があります。 個別に、またはメッセージ サービスの一環として、プロファイルに、サービス プロバイダーを追加するときは、プロファイルに、プロバイダーに適用される、Mapisvc.inf から **[サービス プロバイダー]** セクションのすべてコピーされます。 Mapisvc.inf の構造の詳細については、 [MapiSvc.inf のファイル形式](file-format-of-mapisvc-inf.md)を参照してください。
    
- DLL を読み込むには、 **LoadLibrary**の Windows API 関数を呼び出しています。 MAPI は、初回のみまたはそのいずれかの方法に関係なくかどうかそれが既に読み込まれています) は、サービス プロバイダーの DLL を使用するたびに**LoadLibrary**を呼び出し、ため、サービス ・ プロバイダーを行ってはいけません、読み込まれる回数についての前提条件。 **LoadLibrary**への呼び出しごとに、MAPI が**終わった**とき、サービス ・ プロバイダー DLL が不要になった Windows API 関数の呼び出しです。 
    
- プロバイダーのエントリ ポイント関数を呼び出しています。 MAPI は、ログオン プロセスを開始するは、プロバイダーのエントリ ポイント関数が呼び出されます。 エントリ ポイント関数では、MAPI が使用しているバージョンと互換性のあるサービス プロバイダー インターフェイス (SPI) のバージョンを使用していることを確認します。 これらの関数は、新しく作成したプロバイダーのオブジェクトにポインターを返します。 エントリの作成の詳細については関数を使用してプロバイダーのポイントは、[サービス プロバイダーのエントリ ポイント関数を実装する](implementing-a-service-provider-entry-point-function.md)を参照してください。
    
## <a name="see-also"></a>関連項目



[MAPI サービス プロバイダー](mapi-service-providers.md)

