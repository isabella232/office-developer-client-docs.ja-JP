---
title: エントリの識別子を構築します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1d38c0ac7ddbd24123dd51d7315644f3ad786d15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799807"
---
# <a name="constructing-entry-identifiers"></a>エントリの識別子を構築します。

  
  
**適用されます**: Outlook 
  
エントリ id は、[エントリ ID](entryid.md)の構造で構成されます。 **エントリ ID**の構造は、エントリ id と、実際のエントリの識別子の属性を記述するフラグで構成されます。 
  
## <a name="entryid-structure"></a>エントリ ID の構造

**エントリ ID**の構造体の定義は次のとおりです。 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

MAPI_DIM は、MapiDefs.h ヘッダー ファイルで定義されている定数です。 
  
4 バイトの**abFlags**メンバーの最初のバイトは種類を説明のエントリ id を使用し、次の値を持つことができます。 
  
- MAPI_NOTRECI-エントリの識別子を示します、メッセージの受信者として使用できません。
    
- MAPI_NOTRESERVED-エントリ id を他のユーザーがアクセスできないことを示します。
    
- MAPI_NOW-別のタイミングでのエントリ id を使用できないということを示します。
    
- MAPI_SHORTTERM-短期的なエントリの識別子であることを示します。 エントリの識別子の他の使用が許可されていない限り、このバイトで他のすべての値を設定しなければなりません。
    
- MAPI_THISSESSION-他のセッションのエントリ id を使用できないということを示します。
    
- MAPI_NOTRESERVED-その他のオブジェクトのエントリ id が他のサービス プロバイダーによって使用できることをことを示します。
    
アドレス帳、メッセージ ストア プロバイダーによって作成されたエントリの識別子の**ab**のメンバーは 2 つの要素で構成します。 オブジェクトを識別する、サービス ・ プロバイダー、および 1 つを識別する 16 バイトの[MAPIUID](mapiuid.md)構造体です。 **MAPIUID**は、グローバルに一意の識別子または GUID を格納する構造体です。 GUID は、Microsoft Visual Studio の *[GUID の作成*を使用して作成することができるバイト オーダーに依存しない識別子を * ツールです。 
  
サービス プロバイダーは、 [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)メソッドの呼び出しでのログオン プロセス中に、MAPI との**MAPIUID**構造体を登録します。 クライアントがオブジェクトへのアクセス、 **OpenEntry**メソッドを呼び出すと、MAPI はサービス プロバイダーは、そのアクセスを提供できるかを決定するのに**MAPIUID**構造体を使用します。 サービス プロバイダーは、その DLL のすべてのバージョンの**MAPIUID**と同じ構造を使用する必要があります。 これにより、新しいバージョンのクライアントが応答メッセージを送信し、以前のバージョンで保存します。 
  
16 バイトの**MAPIUID**の後の**ab**のメンバーの残りの部分には、特定のオブジェクトを識別するためのサービス ・ プロバイダーに固有のバイナリ データが含まれています。 エントリ id のこの部分のサイズは固定されていません。 理由内の任意のサイズを指定できます。 通常、サービス プロバイダーには、そのエントリ id のこの部分の次の情報が含まれます。 
  
- バージョン情報、バージョンのエントリ id の形式を変更するのにはサービス ・ プロバイダーの一般的なので、バージョン情報を格納するによって、任意のエントリの識別子を判別する方法をすぐに確認します。
    
- 場所情報-場所の情報は、データ サービス プロバイダーのエントリの識別子によって表されるオブジェクトを検索する方法を示すインジケーターを提供します。 たとえば、サービス プロバイダーは、ディスク オブジェクトが格納されたデータ ファイル内の最後の場所のオフセットを格納できます。 この種の情報は、時間の経過とともに変更できます、ために、サービス プロバイダーは、それらのエントリの識別子でオブジェクトを検索するため複数の方法を提供する必要があります。
    
サービス プロバイダーは、それらのエントリの識別子をリサイクルできるが、この方法は避けてください。 エントリ識別子を再利用する必要がある場合、サービス プロバイダーは最初の使用は、可能な限り再利用するまでに経過するまでの時間をする必要があります。 同じ種類の別のオブジェクトのエントリ id を再割り当てする必要があります。 特定のエントリの識別子をメッセージから開始し、フォルダーに関連付けられている必要がありますできません。
  
## <a name="see-also"></a>関連項目



[MAPI エントリの識別子](mapi-entry-identifiers.md)
