---
title: 機能の XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: (OSC) プロバイダーの XML スキーマ内の機能要素では、OSC プロバイダーの機能を指定することができます。 このような機能には次のものが含まれています。
ms.openlocfilehash: 8192c4d559ae656cfc3b12cd8f50f7d4acd5ed5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804461"
---
# <a name="xml-for-capabilities"></a>機能の XML

(OSC) プロバイダーの XML スキーマ内の**機能**要素では、OSC プロバイダーの機能を指定することができます。 このような機能には次のものが含まれています。 
  
- かどうかを取得する、キャッシュ、または動的に友人や活動を検索、ソーシャル ネットワークからプロバイダーをサポートします。
    
- 方法、OSC では、特定のログオン ユーザー インターフェイスが表示されます。
    
- かどうか、OSC はフォーム ベース認証を使用して、または、ソーシャル ネットワーク上のユーザーに、ソーシャル ネットワークとログを自動的に構成する必要があります。
    
**機能**の XML スキーマは、プロバイダーがサポートする機能が、OSC に特定されるために重要です。 OSC プロバイダーでは、_結果_の文字列を返す[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドを実装する必要があります。 OSC では、**機能**要素の XML スキーマ定義に準拠している_結果_の文字列の OSC プロバイダーの機能に関する情報を取得する**ISocialProvider::GetCapabilities**を呼び出します。 この情報は、それ以降、OSC から OSC プロバイダーが正常に動作するを使用できます。 
  
OSC プロバイダーの機能を**ISocialProvider::GetCapabilities**メソッドの出力パラメーターとして指定するには、OSC プロバイダーの拡張機能の XML スキーマに準拠する必要があります。 **機能**の XML データ構造を次の図に示します。 
  
**図 1 です。\<機能\>[XML データ構造**

![機能 XML の構造](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
**機能**要素の子要素の詳細な説明については、[機能の XML 要素](capabilities-xml-elements.md)を参照してください。 XML の**機能**の使用例は、[機能の XML の例](capabilities-xml-example.md)を参照してください。 のどの要素には、必須またはオプションを含む、OSC プロバイダーの XML スキーマの完全な定義は、 [Outlook ソーシャル コネクタ プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)を参照してください。
  
## <a name="see-also"></a>関連項目

- [機能の XML の例](capabilities-xml-example.md)  
- [友人や活動を同期します。](synchronizing-friends-and-activities.md)  
- [友人の XML](xml-for-friends.md)  
- [活動の XML](xml-for-activities.md)
- [OSC の XML スキーマを使用してプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)

