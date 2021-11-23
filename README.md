# workflow
Asyncronous Parralel Networking and Computing Engine
A server engine that allows you to holistically integrate your tasks including all search services, cloud input method, online advertisements, etc., handling more than 100 000 requests per second. This is an enterprise-level programming engine based on Sogou's server engine in light and elegant design which can satisfy most C++ back-end development requirements. 
Common use cases include (but not limited to) : 
1. Building an HTTP server with a multifunctional asynchronous client,currently supporting HTTP, Redis, MySQL and Kafka protocols.
2. Service governance, a seamless mechanism to manage the services we depend on
3. An algorithm factory, which provides some common computing tasks, such as sorting, merging, etc.
4. Parallel Ligtning Network Smart Contract deployment on the mainnet

System design features

    Protocol
        In most cases, users use built-in common network protocols, such as HTTP, Redis or various rpc.
        Users can also easily customize user-defined network protocol. In the customization, they only need to provide serialization and deserialization functions to define their own client/server.
    Algorithm
        In our design, the algorithm is a concept symmetrical to the protocol.
            If protocol call is rpc, then algorithm call is an apc (Async Procedure Call).
        We have provided some general algorithms, such as sort, merge, psort, reduce, which can be used directly.
        Compared with a user-defined protocol, a user-defined algorithm is much more common. Any complicated computation with clear boundaries should be packaged into an algorithm.
    Workflow
        Workflow is the actual business logic, which is to put the protocols and algorithms into the flow graph for use.
        The typical workflow is a closed series-parallel graph. Complex business logic may be a non-closed DAG.
        The workflow graph can be constructed directly or dynamically generated based on the results of each step. All tasks are executed asynchronously.



Usage

    git clone https://github.com/mac-oya/workflow
make
    make



