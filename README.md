# PhoenixTask

USE [PHOENIX_TASK]
GO

/****** Object:  Table [dbo].[ACCOUNT_TRANSACTIONS]    Script Date: 16/01/2025 09:29:46 ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

--create ACCOUNT_TRANSACTION table
CREATE TABLE [dbo].[ACCOUNT_TRANSACTIONS](
	[TransactionId] [int] IDENTITY(1,1) NOT NULL,
	[FullName] [nvarchar](255) NULL,
	[EnglishFullName] [nvarchar](255) NULL,
	[DateOfBirth] [datetime] NULL,
	[UserId] [char](9) NOT NULL,
	[OperationId] [int] NOT NULL,
	[AccountNumber] [varchar](20) NOT NULL,
	[Amount] [decimal](18, 0) NOT NULL,
	[TransactionDate] [datetime] NULL,
PRIMARY KEY CLUSTERED 
(
	[TransactionId] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON, OPTIMIZE_FOR_SEQUENTIAL_KEY = OFF) ON [PRIMARY]
) ON [PRIMARY]


--create OPERATIONS_TYPE table
CREATE TABLE [dbo].[OPERATIONS_TYPE](
	[OperationId] [int] NOT NULL,
	[OperationDesc] [nvarchar](50) NOT NULL,
PRIMARY KEY CLUSTERED 
(
	[OperationId] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON, OPTIMIZE_FOR_SEQUENTIAL_KEY = OFF) ON [PRIMARY]
) ON [PRIMARY]


GO

Connect the DB in appsettings.json
"DefaultConnection": "Server=yourServerName;Database=PHOENIX_TASK;Trusted_Connection=True;User Id=yuorUserId;Password=yourPassword;TrustServerCertificate=True;"

