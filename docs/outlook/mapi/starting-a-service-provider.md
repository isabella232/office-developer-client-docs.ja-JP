---
title: サービス プロバイダーの開始
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: f67976681ef0283c86e1c09c49e531572668ff50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439556"
---
# <a name="starting-a-service-provider"></a>サービス プロバイダーの開始

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントが MAPI とのセッションを開始した後のある時点で、サービス プロバイダーが開始されます。 トランスポート プロバイダーは、クライアントがサービスの要求を行う際に開始されます。 アドレス帳とメッセージ ストア プロバイダーは、クライアントのログオン プロセス中に開始されます。
  
クライアントは [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) を呼び出して、プロファイルに含まれる各アドレス帳プロバイダーと [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) を読み込み、特定のメッセージ ストア プロバイダーを読み込む。 メッセージ サービスの一部であるアドレス帳プロバイダーは、サービス内の他のプロバイダーの前に開始されます。 
  
MAPI は、次の手順を実行して、アクティブ なプロファイル内の各サービス プロバイダーを開始します。
  
- プロファイル内の DLL の名前を検索します。 プロバイダー DLL がプロファイルに表示されるのを確認するには、Mapisvc.inf 構成ファイルにプロバイダー DLL の名前を登録する必要があります。 サービス プロバイダーが個別に、またはメッセージ サービスの一部としてプロファイルに追加される場合、プロバイダーに適用される Mapisvc.inf の [サービス プロバイダー **]** セクションはすべてプロファイルにコピーされます。 Mapisvc.inf の構造の詳細については [、「MapiSvc.inf のファイル形式」を参照してください](file-format-of-mapisvc-inf.md)。
    
- DLL を読みWindows API 関数 **LoadLibrary** を呼び出します。 MAPI は、(既に読み込まれているかどうかに関係なく) サービス プロバイダー DLL を使用する度に **LoadLibrary** を呼び出すので、サービス プロバイダーは、読み込まれる回数を前提としなくする必要があります。 **LoadLibrary** を呼び出すごとに、MAPI はサービス プロバイダー DLL が不要になったWindows API 関数 **FreeLibrary** を呼び出します。 
    
- プロバイダーのエントリ ポイント関数を呼び出します。 MAPI は、ログオン プロセスを開始するためにプロバイダーのエントリ ポイント関数を呼び出します。 エントリ ポイント関数は、MAPI で使用されているバージョンと互換性のあるバージョンのサービス プロバイダー インターフェイス (SPI) を使用している必要があります。 これらの関数は、新しく作成されたプロバイダー オブジェクトへのポインターも返します。 プロバイダーのエントリ ポイント関数の作成の詳細については、「Service Provider Entry Point Function の実装」 [を参照してください](implementing-a-service-provider-entry-point-function.md)。
    
## <a name="see-also"></a>関連項目



[MAPI サービス プロバイダー](mapi-service-providers.md)

