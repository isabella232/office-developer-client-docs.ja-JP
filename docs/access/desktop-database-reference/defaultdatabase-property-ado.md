---
title: DefaultDatabase プロパティ (ADO)
TOCTitle: DefaultDatabase property (ADO)
ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15)
ms:contentKeyID: 48546784
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5579e132f4fc58594e1fece841e98557ab8b7fb2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589667"
---
# <a name="defaultdatabase-property-ado"></a>DefaultDatabase プロパティ (ADO)


**適用先**: Access 2013、Office 2013

[Connection](connection-object-ado.md) オブジェクトの既定のデータベースを示します。

## <a name="settings-and-return-values"></a>設定および戻り値

プロバイダーで使用可能なデータベースの名前に評価される文字列型 (**String**) の値を設定または取得します。

## <a name="remarks"></a>注釈

**DefaultDatabase** プロパティは、特定の **Connection** オブジェクトの既定のデータベースの名前を設定または取得するために使います。

既定のデータベースがある場合、そのデータベースのオブジェクトにアクセスする SQL 文の構文が不適切な場合があります。 **DefaultDatabase** プロパティで指定されたデータベース以外のデータベースのオブジェクトにアクセスするには、オブジェクト名を目的のデータベース名で修飾する必要があります。接続時に、プロバイダーは **DefaultDatabase** プロパティに既定のデータベース情報を書き込みます。プロバイダーの中には 1 つの接続に 1 つのデータベースしか許可しないものがあり、その場合は **DefaultDatabase** プロパティを変更できません。

データ ソースとプロバイダーによっては、この機能をサポートせず、エラーまたは空の文字列を返す場合があります。

**リモート データ サービスの使用状況** このプロパティは、クライアント側の Connection オブジェクト **では使用** できません。

