Atlas atlas-104b3m-shard-0 [primary] PCEA24CY002> db.getName()
PCEA24CY002
Atlas atlas-104b3m-shard-0 [primary] PCEA24CY002> db.hello()
| 
{
  topologyVersion: { processId: ObjectId('6ae0b337c78fb97b2f1f984a'), counter: Long('6') },
  hosts: [
    'ac-28kwaq2-shard-00-00.u5gi0my.mongodb.net:27017',
    'ac-28kwaq2-shard-00-01.u5gi0my.mongodb.net:27017',
    'ac-28kwaq2-shard-00-02.u5gi0my.mongodb.net:27017'
  ],
  setName: 'atlas-104b3m-shard-0',
  setVersion: 367,
  isWritablePrimary: true,
  secondary: false,
  primary: 'ac-28kwaq2-shard-00-02.u5gi0my.mongodb.net:27017',
  tags: {
    workloadType: 'OPERATIONAL',
    provider: 'AWS',
    nodeType: 'ELECTABLE',
    diskState: 'READY',
    cacheState: 'READY',
    availabilityZone: 'aps1-az2',
    region: 'AP_SOUTH_1'
  },
  me: 'ac-28kwaq2-shard-00-02.u5gi0my.mongodb.net:27017',
  electionId: ObjectId('7fffffff00000000000003b9'),
  lastWrite: {
    opTime: { ts: Timestamp({ t: 1793157742, i: 8 }), t: Long('953') },
    lastWriteDate: ISODate('2026-10-28T03:22:22.000Z'),
    majorityOpTime: { ts: Timestamp({ t: 1793157742, i: 8 }), t: Long('953') },
    majorityWriteDate: ISODate('2026-10-28T03:22:22.000Z')
  },
  maxBsonObjectSize: 16777216,
  maxMessageSizeBytes: 48000000,
  maxWriteBatchSize: 100000,
  localTime: ISODate('2026-10-28T03:22:22.738Z'),
  logicalSessionTimeoutMinutes: 30,
  connectionId: 15090,
  minWireVersion: 0,
  maxWireVersion: 25,
  readOnly: false,
  ok: 1,
  '$clusterTime': {
    clusterTime: Timestamp({ t: 1793157742, i: 8 }),
    signature: {
      hash: Binary.createFromBase64('6DJbTf1YmOCJEbMamMVqKJ+HfFs=', 0),
      keyId: Long('7664981700832657417')
    }
  },
  operationTime: Timestamp({ t: 1793157742, i: 8 })
}
Atlas atlas-104b3m-shard-0 [primary] PCEA24CY002> rs.status()
{
  set: 'atlas-104b3m-shard-0',
  date: ISODate('2026-10-28T03:22:32.204Z'),
  myState: 1,
  term: Long('953'),
  syncSourceHost: '',
  syncSourceId: -1,
  heartbeatIntervalMillis: Long('2000'),
  majorityVoteCount: 2,
  writeMajorityCount: 2,
  votingMembersCount: 3,
  writableVotingMembersCount: 3,
  optimes: {
    lastCommittedOpTime: { ts: Timestamp({ t: 1793157752, i: 2 }), t: Long('953') },
    lastCommittedWallTime: ISODate('2026-10-28T03:22:32.180Z'),
    readConcernMajorityOpTime: { ts: Timestamp({ t: 1793157752, i: 2 }), t: Long('953') },
    appliedOpTime: { ts: Timestamp({ t: 1793157752, i: 2 }), t: Long('953') },
    durableOpTime: { ts: Timestamp({ t: 1793157752, i: 2 }), t: Long('953') },
    writtenOpTime: { ts: Timestamp({ t: 1793157752, i: 2 }), t: Long('953') },
    lastAppliedWallTime: ISODate('2026-10-28T03:22:32.180Z'),
    lastDurableWallTime: ISODate('2026-10-28T03:22:32.180Z'),
    lastWrittenWallTime: ISODate('2026-10-28T03:22:32.180Z')
  },
  lastStableRecoveryTimestamp: Timestamp({ t: 1793157696, i: 3 }),
  electionCandidateMetrics: {
    lastElectionReason: 'stepUpRequestSkipDryRun',
    lastElectionDate: ISODate('2026-10-27T14:22:13.410Z'),
    electionTerm: Long('953'),
    lastCommittedOpTimeAtElection: { ts: Timestamp({ t: 1793110933, i: 1 }), t: Long('952') },
    lastSeenWrittenOpTimeAtElection: { ts: Timestamp({ t: 1793110933, i: 1 }), t: Long('952') },
    lastSeenOpTimeAtElection: { ts: Timestamp({ t: 1793110933, i: 1 }), t: Long('952') },
    numVotesNeeded: 2,
    priorityAtElection: 7,
    electionTimeoutMillis: Long('5000'),
    priorPrimaryMemberId: 1,
    numCatchUpOps: Long('0'),
    newTermStartDate: ISODate('2026-10-27T14:22:13.477Z'),
    wMajorityWriteAvailabilityDate: ISODate('2026-10-27T14:22:13.575Z')
  },
  members: [
    {
      _id: 0,
      name: 'ac-28kwaq2-shard-00-00.u5gi0my.mongodb.net:27017',
      health: 1,
      state: 2,
      stateStr: 'SECONDARY',
      uptime: 46839,
      optime: { ts: Timestamp({ t: 1793157751, i: 17 }), t: Long('953') },
      optimeDurable: { ts: Timestamp({ t: 1793157751, i: 17 }), t: Long('953') },
      optimeWritten: { ts: Timestamp({ t: 1793157751, i: 17 }), t: Long('953') },
      optimeDate: ISODate('2026-10-28T03:22:31.000Z'),
      optimeDurableDate: ISODate('2026-10-28T03:22:31.000Z'),
      optimeWrittenDate: ISODate('2026-10-28T03:22:31.000Z'),
      lastAppliedWallTime: ISODate('2026-10-28T03:22:32.180Z'),
      lastDurableWallTime: ISODate('2026-10-28T03:22:32.180Z'),
      lastWrittenWallTime: ISODate('2026-10-28T03:22:32.180Z'),
      lastHeartbeat: ISODate('2026-10-28T03:22:32.079Z'),
      lastHeartbeatRecv: ISODate('2026-10-28T03:22:31.885Z'),
      pingMs: Long('0'),
      lastHeartbeatMessage: '',
      syncSourceHost: 'ac-28kwaq2-shard-00-02.u5gi0my.mongodb.net:27017',
      syncSourceId: 2,
      infoMessage: '',
      configVersion: 367,
      configTerm: 953
    },
    {
      _id: 1,
      name: 'ac-28kwaq2-shard-00-01.u5gi0my.mongodb.net:27017',
      health: 1,
      state: 2,
      stateStr: 'SECONDARY',
      uptime: 46728,
      optime: { ts: Timestamp({ t: 1793157751, i: 5 }), t: Long('953') },
      optimeDurable: { ts: Timestamp({ t: 1793157751, i: 5 }), t: Long('953') },
      optimeWritten: { ts: Timestamp({ t: 1793157751, i: 5 }), t: Long('953') },
      optimeDate: ISODate('2026-10-28T03:22:31.000Z'),
      optimeDurableDate: ISODate('2026-10-28T03:22:31.000Z'),
      optimeWrittenDate: ISODate('2026-10-28T03:22:31.000Z'),
      lastAppliedWallTime: ISODate('2026-10-28T03:22:32.180Z'),
      lastDurableWallTime: ISODate('2026-10-28T03:22:32.180Z'),
      lastWrittenWallTime: ISODate('2026-10-28T03:22:32.180Z'),
      lastHeartbeat: ISODate('2026-10-28T03:22:31.216Z'),
      lastHeartbeatRecv: ISODate('2026-10-28T03:22:31.910Z'),
      pingMs: Long('0'),
      lastHeartbeatMessage: '',
      syncSourceHost: 'ac-28kwaq2-shard-00-02.u5gi0my.mongodb.net:27017',
      syncSourceId: 2,
      infoMessage: '',
      configVersion: 367,
      configTerm: 953
    },
    {
      _id: 2,
      name: 'ac-28kwaq2-shard-00-02.u5gi0my.mongodb.net:27017',
      health: 1,
      state: 1,
      stateStr: 'PRIMARY',
      uptime: 46913,
      optime: { ts: Timestamp({ t: 1793157752, i: 2 }), t: Long('953') },
      optimeDate: ISODate('2026-10-28T03:22:32.000Z'),
      optimeWritten: { ts: Timestamp({ t: 1793157752, i: 2 }), t: Long('953') },
      optimeWrittenDate: ISODate('2026-10-28T03:22:32.000Z'),
      lastAppliedWallTime: ISODate('2026-10-28T03:22:32.180Z'),
      lastDurableWallTime: ISODate('2026-10-28T03:22:32.180Z'),
      lastWrittenWallTime: ISODate('2026-10-28T03:22:32.180Z'),
      syncSourceHost: '',
      syncSourceId: -1,
      infoMessage: '',
      electionTime: Timestamp({ t: 1793110933, i: 2 }),
      electionDate: ISODate('2026-10-27T14:22:13.000Z'),
      configVersion: 367,
      configTerm: 953,
      self: true,
      lastHeartbeatMessage: ''
    }
  ],
  ok: 1,
  '$clusterTime': {
    clusterTime: Timestamp({ t: 1793157752, i: 2 }),
    signature: {
      hash: Binary.createFromBase64('oVIAFPuysgAMGcTjdwKPAGuSggI=', 0),
      keyId: Long('7664981700832657417')
    }
  },
  operationTime: Timestamp({ t: 1793157752, i: 2 })
}
Atlas atlas-104b3m-shard-0 [primary] PCEA24CY002> use PCEA24CY002
| 
| db.replication_lab.insertOne(
|   {
|     testId: "replication-001",
|     message: "Testing replication",
|     createdAt: new Date()
|   },
|   {
|     writeConcern: {
|       w: "majority",
|       wtimeout: 5000
|     }
|   }
| )
already on db PCEA24CY002
Atlas atlas-104b3m-shard-0 [primary] PCEA24CY002> db.replication_lab.insertOne(
|   {
|     testId: "replication-001",
|     message: "Testing replication",
|     createdAt: new Date()
|   },
|   {
|     writeConcern: {
|       w: "majority",
|       wtimeout: 5000
|     }
|   }
| )
{
  acknowledged: true,
  insertedId: ObjectId('6ae16ad8e81d1f3274a30b15')
}
Atlas atlas-104b3m-shard-0 [primary] PCEA24CY002> db.replication_lab.findOne({
|   testId: "replication-001"
| })
{
  _id: ObjectId('6ae16ad8e81d1f3274a30b15'),
  testId: 'replication-001',
  message: 'Testing replication',
  createdAt: ISODate('2026-10-28T03:24:08.157Z')
}
Atlas atlas-104b3m-shard-0 [primary] PCEA24CY002> 
