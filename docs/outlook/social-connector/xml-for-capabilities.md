---
title: 機能の XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: (OSC) プロバイダー XML スキーマの capabilities 要素を使用すると、OSC プロバイダーは機能を指定できます。 このような機能には、次の機能が含まれます。
ms.openlocfilehash: 6b46567853a2f8a37ff5f9479c9eb8e4f4da7ccf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582982"
---
# <a name="xml-for-capabilities"></a>機能の XML

(OSC) プロバイダー XML スキーマの **capabilities** 要素を使用すると、OSC プロバイダーは機能を指定できます。 このような機能には、次の機能が含まれます。 
  
- プロバイダーがソーシャル ネットワークからのフレンドやアクティビティの取得、キャッシュ、または動的な参照をサポートするかどうか。
    
- OSC が特定のログオン ユーザー インターフェイスを表示する方法。
    
- OSC がフォーム ベース認証を使用するか、ソーシャル ネットワークを自動的に構成し、ソーシャル ネットワーク上のユーザーにログオンするか。
    
機能の XML スキーマ **は、** プロバイダーがサポートする機能を OSC に識別するために重要です。 OSC プロバイダーは、結果文字列を返す [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) メソッドを実装する  _必要_ があります。 OSC は **ISocialProvider::GetCapabilities** を呼び出して、結果文字列内の OSC プロバイダーの機能に関する情報を取得します。この情報は、capabilities 要素の XML スキーマ定義に準拠しています。   この情報により、OSC から OSC プロバイダーへの後続の呼び出しが正しく動作します。 
  
**ISocialProvider::GetCapabilities** メソッドの出力パラメーターとして OSC プロバイダーの機能を指定するには、OSC プロバイダー拡張 XML スキーマに準拠する必要があります。 次の図は、機能 **XML 構造を** 示しています。 
  
**図 1. \<capabilities\> XML 構造**

![機能 XML の構造](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
capabilities 要素の子要素の詳細な説明については[、「Capabilities XML Elements」を参照してください](capabilities-xml-elements.md)。 機能 XML の例 **については、「Capabilities** [XML の例」を参照してください](capabilities-xml-example.md)。 OSC プロバイダー XML スキーマの完全な定義 (必須または省略可能な要素を含む) については、「ソーシャル コネクタ プロバイダー XML スキーマOutlook[を参照してください](outlook-social-connector-provider-xml-schema.md)。
  
## <a name="see-also"></a>関連項目

- [機能 XML の例](capabilities-xml-example.md)  
- [フレンドとアクティビティの同期](synchronizing-friends-and-activities.md)  
- [友人のための XML](xml-for-friends.md)  
- [アクティビティの XML](xml-for-activities.md)
- [OSC XML スキーマを使用したプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)

