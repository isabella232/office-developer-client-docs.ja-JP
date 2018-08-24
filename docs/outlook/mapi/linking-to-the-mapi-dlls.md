---
title: MAPI DLL へのリンク
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 428e92dd783368374fa07c8df9629d60e83dd217
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582029"
---
# <a name="linking-to-the-mapi-dlls"></a>MAPI DLL へのリンク

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI クライアントにリンクできます MAPI Dll、暗黙的にまたは明示的に Windows 関数**LoadLibrary**と**GetProcAddress**を使用しています。 MAPI Dll を明示的にリンクする方法の詳細については、 [MAPI の関数へのリンク](how-to-link-to-mapi-functions.md)を参照してください。
  
MAPI には、MAPIX の種類の定義ステートメントが用意されています。H のヘッダー ファイルの次の関数の:
  
[MAPILogonEx](mapilogonex.md)
  
[MAPIUninitialize](mapiuninitialize.md)
  
[MAPIInitialize](mapiinitialize.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAdminProfiles](mapiadminprofiles.md)
  
MAPI Dll に明示的にリンクする場合に正しく対応するエントリ ポイントを呼び出すには、これらの型定義を使用します。
  
サービス プロバイダーは、非 MAPI 機能を含めることができます-は、MAPI とはまったく関係のない機能-その DLL にします。 これらの機能を使用する場合は、 **LoadLibrary**を使用した後、DLL をメモリから削除するのには**終わった**DLL を使用する前に呼び出します。 MAPI がサービス ・ プロバイダー DLL の MAPI 以外の使用方法を認識しないので、DLL が必要なときに利用できるという保証はありません。 MAPI は、不要になったすべてのクライアントにサービスを必要とするアクティブなセッションがある場合に、サービス プロバイダーの DLL を解放します。 
  

