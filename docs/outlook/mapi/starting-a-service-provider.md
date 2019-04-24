---
title: サービスプロバイダーの開始
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: f67976681ef0283c86e1c09c49e531572668ff50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341714"
---
# <a name="starting-a-service-provider"></a>サービスプロバイダーの開始

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントが MAPI を使用してセッションを開始した後のある時点では、サービスプロバイダーが開始されます。 クライアントがサービスに対して要求を行うと、トランスポートプロバイダーが開始されます。 アドレス帳およびメッセージストアプロバイダーは、クライアントのログオンプロセス中に開始されます。
  
クライアントは[imapisession:: OpenAddressBook](imapisession-openaddressbook.md)を呼び出して、プロファイルに含まれている各アドレス帳プロバイダーと[imapisession:: openmsgstore](imapisession-openmsgstore.md)を読み込んで、特定のメッセージストアプロバイダーを読み込みます。 メッセージサービスの一部であるアドレス帳プロバイダーは、サービス内の他のプロバイダーよりも前に開始されます。 
  
MAPI は、アクティブなプロファイルで各サービスプロバイダーを開始します。そのためには、次の手順を実行します。
  
- プロファイルに DLL の名前を配置する。 mapisvc.inf 構成ファイルにプロバイダー DLL の名前を登録して、プロファイルに表示されるようにする必要があります。 サービスプロバイダーがプロファイルに個別に、またはメッセージサービスの一部として追加されると、プロバイダーに適用される mapisvc.inf の **[サービスプロバイダ]** セクションすべてがプロファイルにコピーされます。 mapisvc.inf の構造の詳細については、「 [mapisvc.inf のファイル形式](file-format-of-mapisvc-inf.md)」を参照してください。
    
- DLL を読み込むために**** Windows API 関数を呼び出しています。 MAPI は、 **** (既に読み込まれているかどうかにかかわらず) サービスプロバイダ DLL を使用するたびに、または初めて実行した場合には、サービスプロバイダーがロードされる回数を想定しないようにする必要があります。 **LoadLibrary**へのすべての呼び出しでは、サービスプロバイダー DLL が不要になったときに、MAPI が Windows API 関数**FreeLibrary**を呼び出すことになります。 
    
- プロバイダーのエントリポイント関数を呼び出しています。 MAPI は、プロバイダーのエントリポイント関数を呼び出して、ログオンプロセスを開始します。 エントリポイント関数 MAPI で使用されているバージョンと互換性のあるバージョンのサービスプロバイダインターフェイス (SPI) を使用していることを確認します。 これらの関数は、新しく作成されたプロバイダオブジェクトへのポインターも返します。 プロバイダー用のエントリポイント関数を作成する方法の詳細については、「[サービスプロバイダーエントリポイント関数の実装](implementing-a-service-provider-entry-point-function.md)」を参照してください。
    
## <a name="see-also"></a>関連項目



[MAPI サービスプロバイダー](mapi-service-providers.md)

