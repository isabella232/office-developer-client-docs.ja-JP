---
title: defaultdatabase プロパティ (ADO)
TOCTitle: DefaultDatabase property (ADO)
ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15)
ms:contentKeyID: 48546784
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 01ca42ff738afe3a35cab6263cdae32ac256f3d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294149"
---
# <a name="defaultdatabase-property-ado"></a>defaultdatabase プロパティ (ADO)


**適用先:** Access 2013、Office 2013

[Connection](connection-object-ado.md) オブジェクトの既定のデータベースを示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

プロバイダーで使用可能なデータベースの名前に評価される文字列型 (**String**) の値を設定または取得します。

## <a name="remarks"></a>注釈

**DefaultDatabase** プロパティは、特定の **Connection** オブジェクトの既定のデータベースの名前を設定または取得するために使います。

既定のデータベースがある場合、そのデータベースのオブジェクトにアクセスする SQL 文の構文が不適切な場合があります。 **DefaultDatabase** プロパティで指定されたデータベース以外のデータベースのオブジェクトにアクセスするには、オブジェクト名を目的のデータベース名で修飾する必要があります。接続時に、プロバイダーは **DefaultDatabase** プロパティに既定のデータベース情報を書き込みます。プロバイダーの中には 1 つの接続に 1 つのデータベースしか許可しないものがあり、その場合は **DefaultDatabase** プロパティを変更できません。

データ ソースとプロバイダーによっては、この機能をサポートせず、エラーまたは空の文字列を返す場合があります。

**リモートデータサービスの使用状況**このプロパティは、クライアント側の**Connection**オブジェクトでは使用できません。

